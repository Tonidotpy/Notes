---
 Created: 2022-12-27 17:01
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [ICMP]
 Tags: [protocol]
---

**Internet Control Message Protocol** (*ICMP*) è un protocollo di rete utilizzato dai sistemi operativi per inviare **messaggi di controllo** e **segnalazione di errori** tra i dispositivi connessi a una rete

---

Questo protocollo viene utilizzato per **notificare errori** alla sorgente di un datagramma ed é un ottimo strumento per la **gestione** e **manutenzione** delle reti
Se un messaggio ICMP genera un errore non viene generato nessun messaggio di errore

ICMP è **interdipendente** con [[Internet Protocol versione 4|IP]] ossia:
- IP ha bisogno di ICMP per segnalare errori
- ICMP si serve di IP per trasportare i messaggi

E i suoi contenuti vengono trasportati come dati all'interno di un datagramma

Un messaggio ICMP ha un header molto semplice:
- **Type** `8 bit`
- **Code** `8 bit`
- **Checksum** `8 bit`

Di seguito vengono rappresentati alcuni possibili valori del campo type:

| Type                              | Descrizione                                                                   |
| --------------------------------- | ----------------------------------------------------------------------------- |
| Destination unreachable           | Il pacchetto non può essere consegnato                                        |
| Port unreachable                  | Nessuno all'host destinatario ascolta sulla porta specificata                 |
| Time exceeded                     | Il campo *TTL* dell'header IP è sceso a `0`                                   |
| Parameter problem                 | Valore non valido in un campo dell'header IP                                  |
| Source quench                     | Chiede alla sorgente di rallentare l'invio di dati                            |
| Redirect                          | Dice al router a quale host inoltrare il datagramma                           |
| Echo and echo reply               | Usati da `ping` per capire se un host è attivo                                |
| Timestamp request/reply           | Come i comandi `echo`, ma per l'orologio locale dei router                    |
| Router advertisement/solicitation | Per proporsi come router, o per chiedere quali router ci sono nelle vicinanze |
| Fragmentation needed              | Flag IP *non frammentare* a `1`, ma il datagramma eccede l'*MTU*                                                                              |
