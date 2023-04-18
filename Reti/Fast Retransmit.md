---
 Created: 2022-12-23 15:43
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **Fast Retransmit** è una tecnica utilizzata in diverse tecnologie di rete per **gestire** la ritrasmissione di pacchetti di dati in caso di **errore** o **perdita** di pacchetti durante la trasmissione

---

Alla ricezione del 3° ACK duplicato **ritrasmettiamo** il segmento indicato dall'ACK (*"fast retransmit"*) e si entra nella fase di [[Fast Recovery]]