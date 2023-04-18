---
 Created: 2022-12-23 15:45
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **Fast Recovery** è una tecnica utilizzata in diverse tecnologie di rete per **gestire** la ripresa del flusso di dati dopo una **perdita** di pacchetti durante la trasmissione

---

Alla ricezione del 3° ACK duplicato **dimezzo** l'[[Slow Start|SSTHRESH]] e imposto la dimensione della [[Finestra di congestione|CWND]] alla sua **metà** più `3`
Se arrivano altri ACK duplicati **incremento** la dimensione della finestra di `1`
Quando arriva un ACK valido imposto la dimensione della CWND **uguale** a SSTHRESH sposto il **puntatore *low*** al primo segmento non ACKed e passo alla fase di [[Congestion Avoidance]]
Altrimenti, sei arriva un ACK parziale, **ritrasmetto** il primo segmento per cui non ho un ACK, **riduco** la dimensione della CWND del numero di segmenti ACKed + `1` e sposto il **puntatore *low*** al primo segmento non ACKed