---
 Created: 2022-12-20 15:53
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **demultiplexing** è il processo inverso del [[Multiplexing|multiplexing]], ovvero la **separazione** di più flussi di dati che sono stati trasmessi sulla stessa **connessione** o sulla stessa **risorsa** di trasmissione

---

In un sistema a layer il demultiplexing utilizza le [[Protocollo|PCI]] nell'header per consegnare i segmenti ricevuti alle socket giuste

---

## Demultiplexing senza connessione

Nel demultiplexing senza connessione la socket [[User Datagram Protocol|UDP]] viene **identificata** tramite l'[[Internet Protocol versione 4|IP]] di destinazione il numero di **porta** di destinazione
Quando l'host rivece il segmento UPD **controlla** che il numero della porta di destinazione e invia il segmento alla socket con quel numero

I datagrammi IP con indirizzi e/o numeri di porta di origine differenti vengono inviati alla stessa socket

## Demultiplexing orientato alla connessione

Nel demultiplexing orientato alla connessione la socket [[Transmission Control Protocol|TCP]] viene identificata tramite gli indirizzi **IP** di origine e destinazione e i **numeri di porta** di origine e destinazione
