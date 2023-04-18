---
 Created: 2022-12-31 19:10
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Wireless LAN, WLAN]
 Tags: []
---

Una **Wireless Local Area Network** (*WLAN*) è una rete di comunicazione **senza fili** che consente ai dispositivi di rete di comunicare tra loro in un'area **limitata**, come un edificio o una stanza

---

Lo **standard** di riferimento per le WLAN è il `802.11`

Una WLAN è formata da:
- Una **stazione wireless** (*STA*): che può essere un qualsiasi nodo della rete
- Un **Basic Service Set** (*BSS*): un gruppo di STA che utilizzano lo stesso canale radio
- Un **Access Point** (*AP*): una stazione integrata nella WLAN e connessa al sistema di distribuzione
- Un **sistema di distribuzione**: che fornisce la connettività verso l'*esterno*
- Un **Extended Service Set** (*ESS*): che unisce più BSS in un'unica rete logica
- Un **portale**: un ponte che si interfaccia verso altre reti

---

In base allo **standard** si possono utilizzare spettri di **frequenze** diverse che possono essere scelte dall'amministratore dell'AP
Un dispositivo che vuole connettersi ad una WLAN ascolta sui canali disponibili alla ricerca di **frame speciali** chiamati *beacon*
Un beacon contiene:
- **Nome della rete**
- **Service Set ID** (*SSID*)
- L'[[Indirizzo MAC|indirizzo MAC]] dell'AP
Una volta trovati degli AP disponibili si può scegliere a quale **associarsi** ed eventualmente **autenticarsi**

Esistono due tipi di **scansioni** per la ricerca di AP:
- **Passiva**:
	- L'AP invia i *beacon*
	- Il dispositivo invia una richiesta di associazione all'AP
	- L'AP risponde con una conferma alla richiesta del dispositivo
- **Attiva**:
	- Il dispositivo invia a tutti i vicini un frame di *probe request*
	- Gli AP rispondono con un *probe response*
	- Seguono una richiesta e conferma di associazione

---

Una WLAN presenta diversi problemi per quanto riguarda i collegamenti:
- La **potenza** del segnale si **attenua** fortemente mentre si propaga
- L'**interferenza** generata dalle fonti che utilizzano le stesse frequenze genera parecchi disturbi del segnale
- La propagazione *multipercorso* del segnale non segue un percorso ben definito e si **riflette** su oggetti e superfici, creando copie che raggiungono il destinatario con ritardi leggermente diversi

Tutto ciò rende il **rilevamento delle collisioni** diventa praticamente impossibile, perciò lo standard `208.11` utilizza [[Carrier Sense Multiple Access Collision Avoidance|CSMA/CA]]

Per un trasmettitore, se il canale di comunicazione rimane **libero** per un tempo chiamato **Distributed Inter-Frame Space** (*DIFS*) viene trasmesso l'intero frame altrimenti si entra in *backoff*
Se il canale risulta occupato (*backoff*) si sceglie un tempo **casuale** da attendere prima di trasmettere
Se non viene ricevuta alcuna risposta, si **aumenta** il valore massimo del tempo di backoff, si sceglie un nuovo tempo e si ripete la procedura

Per un ricevitore, se il frame viene **ricevuto** correttamente viene inviata una risposta dopo un intervallo di tempo chiamato **Short Inter-Frame Space** (*SIFS* < DIFS)

## Problema del terminale nascosto

Il problema del **terminale nascosto** riguarda la connessione tra due terminali `A` e `C` con lo stesso terminale `B`
Entrambi i terminali `A` e `C` *vedono* `B` ma non possono comunicare **direttamente** tra loro a causa di ostacoli o una pesante attenuazione, questo può causare **collisioni** sistematiche

La soluzione è utilizzare il CSMA/CA con un *handshaking* che serve a **prenotare** esplicitamente il canale
Il **trasmettitore** invia una **Request To Send** (*RTS*) mentre il **ricevitore** risponde con un **Clear To Send** (*CTS*)
Il CTS **prenota** il canale per il trasmettitore e notifica la trasmissione ad altre STA, questo può causare però il **problema del terminale esposto**

## Problema del terminale esposto

Il **problema del terminale esposto** riguarda due terminali `A` e `B` che non possono comunicare **direttamente** tra loro ma comunicano con AP diversi
Se il terminale `A` invia un RTS e **occupa** il canale per tutto il tempo impiegato per inviare il messaggio, il terminale `B` viene **bloccato** quando in realtà può inviare messaggi ad un AP diverso da quello con cui sta comunicando `A` senza causare **interferenze**