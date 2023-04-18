---
 Created: 2022-12-25 15:25
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [IPv4, IP]
 Tags: [protocol]
---

**Internet Protocol versione 4** (*IP*) è un protocollo di rete utilizzato per **trasmettere** i pacchetti di dati attraverso [[Internet]] e altre reti di [[Computer|computer]]

---

Ciascun tipo di hardware specifica un limite di dati che una trasmissione può trasportare (**Maximum Transmission Unit**, *MTU*)
Diverse reti possono specificare diverse MTU perciò i datagrammi a volte possono essere troppo grandi per poter essere inviati
Per risolvere questo problema i datagrammi vengono **frammentati** ossia suddivisi in più parti in modo da poter essere inviati ^e2d109

Quando un [[Router|router]] frammenta un messaggio **copia** i campi necessari dell'header e **trasmette** tutti i frammenti in sequenza con identificatori diversi
Inoltre setta delle **flag** in ogni frammento che possono essere:
- **D** (*Do not fragment*): il pacchetto non può più essere frammentato e nel caso viene scartato
- **M** (*More fragments*): serve a segnalare che devono essere ricevuti altri pacchetti per completare il messaggio, è settato a 1 per ogni frammento eccetto l'ultimo

Il messaggio framentato viene poi **riassemblato** solamente una volta raggiunto il destinatario e non prima
Se uno o più frammenti vengono **persi** il protocollo IP prevede un **tempo limite** prima di scartare i frammenti ricevuti memorizzati

>[!FAILURE] Nella realtà la frammentazione a questo livello non viene quasi mai utilizzata in quanto vengono a mancare alcune funzioni di sicurezza che richiedono il datagramma intero per essere applicate

## Datagramma IP

![IP-datagram|450](https://image.slidesharecdn.com/4-protocolloip-090503233603-phpapp01/85/4-protocollo-ip-6-320.jpg?cb=1669126793)

Il datagramma IP è formato da:
- **Ver** (`4 bit`): il numero di versione IP (solo 4 o 6)
- **HLEN** (`4 bit`): la lunghezza dell'header
- **TOS** (`8 bit`): il tipo di servizio (*Type Of Service*)
- **Total length** (`16 bit`): il numero totale di byte nel datagramma, header incluso
- **Fragment Identification** (`16 bit`): numero (di solito sequenziale) assegnato al datagramma che serve ad identificarne il segmento di un messaggio
- **Flags** (`3 bit`): flag utilizzati per capire se il messaggio è frammentato e se il pacchetto è l'ultimo frammento
- **Frag. offset** (`13 bit`): indica in che punto va inserito questo frammento nel messaggio originale
- **TTL** (`8 bit`): un numero che viene ridotto di 1 ad ogni passaggio in router e se rangiugge il valore 0 il datagramma viene scartato e viene inviata una notifica al mittente (*Time To Live*)
- **Protocol** (`8 bit`): il protocollo utilizzato dal livello superiore (es. 6 = TCP, 17 = UDP)
- **Header Checksum** (`16 bit`): un valore utilizzato per controllare la [[Controllo di parità|parità]] dei bit del datagramma
- **Source address** (`32 bit`): [[Indirizzo IPv4|indirizzo IP]] del mittente
- **Destination address** (`32 bit`): indirizzo IP del destinatario
- **Options**: utilizzato in alcuni casi per controllare l'elaborazione e l'instradamento dei datagrammi
- **Padding**: bit a zero aggiunti in modo che l'header sia un multiplo di `32 bit`