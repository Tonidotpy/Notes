---
 Created: 2022-12-28 18:01
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [BGP]
 Tags: [protocol]
---

**Border Gateway Protocol** (*BGP*) è un protocollo di routing utilizzato per **instradare** i pacchetti di dati su reti di [[Computer|computer]]

---

BGP è un ***Path Vector Protocol*** il cui **principio chiave** è quello di lasciare libertà amministrativa per ogni [[Autonomous System|AS]], che può decidere:
- Se pubblicizzare informazioni di raggiungibilità per le proprie reti interne oppure no
- Di ritrarre la raggiungibilità di qualunque propria rete
- Se offrire o meno transito verso altri AS in ogni momento

Ogni AS ha un certo numero di router detti *BGP speaker* che possono parlare attraverso una connessione [[Transmission Control Protocol|TCP]] tra di loro e scambiarsi informazioni sulla raggiungibiltà di altre reti

Le **interconnessioni** tra AS sono controllate da contratti e ne esistono di due tipi:
- **Ingress Policies**: politiche applicate alle rotte che voglio importare nel mio sistema
- **Egress Policies**: politiche applicate alle rotte prima che vengano esportate

I **filtri** controllano ciò che entra ed esce da un AS e possono essere:
- **Ingress filters**
- **Egress filters**

I filtri possono essere **generici** (filtrando un intero AS ad esempio) ma anche **estremamente precisi** (si può filtrare in base ad un qualsiasi campo dei pacchetti)
Se un pacchetto non supera i filtri viene **scartato**

---

Il concetto di *percorso migliore* in BGP è diverso da quello di altri protocolli, in cui si preferiva il percorso **più breve** o con un **costo minore**, ma dipende dalle policy degli AS
Ogni speaker BGP condivide solamente il proprio *best path* per raggiungere una destinazione

>[!ATTENTION] Non è detto che il **best path** sia il percorso più veloce

Per poter risparmiare informazioni, all'interno dei pacchetti generalmente le rotte vengono **aggregate**, si perde però precisione nel percorso

Per le rotte BGP utilizza sostanzialmente tre tabelle:
- **ADJ_RIB_IN**: contiene le rotte che vengono accettate in ingresso e viene usato per valutare percorsi alternativi
- **Routing Table**: contiene i percorsi migliori attuali
- **ADJ_RIB_OUT**: contiene le rotte che hanno superato i filtri in uscita e che devono essere condivise

---

## Messaggi BGP

### Open

É un messaggio utilizzato per aprire una **nuova connessione** con un altro nodo BGP
Se viene accettato il ricevente invia un messaggio di **Keepalive** come conferma e una volta ricevuto la connessione viene considerata **aperta**

![BGP-open-message](https://techhub.hpe.com/eginfolib/networking/docs/switches/3600v2/5998-7619r_l3-ip-rtng_cg/content/images/image69.png)

L'**hold time** è una proposta che si scambiano i due BGP speaker riguardo al **tempo di validità** della rotta (viene utilizzato il minore)
Il **BGP identifier** è l'[[Indirizzo IPv4|indirizzo IP]] identificativo dello speaker che è **uguale** per tutte le interfacce BGP dello speaker

### Notification

É un messaggio utilizzato per **condividere** gli errori

![BGP-notification-message](https://flylib.com/books/2/295/1/html/2/images/1578700892/graphics/02fig47.gif)

Esistono 6 **Error code** in base al tipo di errore e 20 **Error subcodes** in base a dove avviene l'errore

### KeepAlive

É un messaggio utilizzato per **mantenere attiva** (e iniziare) una connessione

I messaggi devono essere inviati in modo tale da non lasciar scadere l'**hold timer** che è stato scelto per la connessione
Possono essere **disattivati** impostando il timer a `0s` e consistono nell'header BGP senza contenuti (`19 Byte`)

### Update

É un messaggio utilizzato per **inoltrare** informazioni di conoscenza

I messaggi contengono **informazioni** di raggiungibilità ed attributi correlati e sono responsabili della **disseminazione** delle informazioni
Le informazioni possono essere di due tipi:
- **Additive**: portano informazioni di raggiungibilità riguardanti nuovi percorsi
- **Sottrattive**: rimuovono percorsi per raggiungere una destinazione

La **rimozione** di una rotta viene chiamata *withdraw*
All'interno di un pacchetto di update vi è una sezione apposita per le rotte che vengono cancellate e viene propagato quando non vi è più un percorso disponibile verso un certo AS

Nel caso in cui un nodo BGP conoscesse un **percorso alternativo** per raggiungere una rotta portebbe decidere di:
- **Rimuovere** la rotta precedente
- **Utilizzare** il nuovo percorso e condividerlo (*Implicit withdraw*)