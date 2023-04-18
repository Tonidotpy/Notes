---
 Created: 2022-12-21 16:03
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [UDP]
 Tags: [protocol]
---

Lo **User Datagram Protocol** (*UDP*) è un protocollo di **trasmissione** dei dati utilizzato nella rete internet che permette di inviare dei messaggi o dei pacchetti di dati da un host a un altro **senza** stabilire una **connessione** di rete esplicita

---

Il protocollo UDP non stabilisce una connessione diretta, che potrebbe aggiungere ritardo, e per questo i segmenti UDP possono essere **perduti** o consegnati **fuori sequenza** all'applicazione
Per questo UDP viene utilizzato principalmente per le applicazioni multimediali, il [[Domain Name System|DNS]] e l'[[Simple Network Management Protocol|SNMP]] in quanto tollerano piccole perdite e sono sensibili alla frequenza

É un tipo di protocollo molto **semplice** i cui header dei segmenti sono molto **corti**
Non ha nessun mezzo per controllare la **congestione** della rete

---

## Datagramma UDP

![UDP-datagram](http://www.programmiamo.altervista.org/internet/immagini/UDP%20Datagram%20Picture.JPG)

Il campo **Checksum** del datagramma UDP serve a rilevare gli **errori** (*bit alterati*) nel segmento trasmesso
La checksum non rileva tutti gli errori possibili ma solo alcuni

Il **mittente** tratta il contenuto del messaggio come una sequenza di numeri da `16 bit`
La checksum non è altro che la somma di tutte le parole (*word*) da `16 bit` in [[Complemento a 1|complemento a 1]]

Il **ricevente** somma tutte le parole del segmento (incluso il checksum) e controlla se il risultato è uguale a `0xFF` ossia 16  bit a `1`
Nel caso non fosse così viene rilevato un errore, altrimenti il datagramma viene considerato corretto (ma non è detto che lo sia davvero)