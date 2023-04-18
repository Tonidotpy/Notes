---
 Created: 2022-12-22 18:59
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [AIMD]
 Tags: []
---

L'**Additive Increase, Multiplicative Decrease** (*AIMD*) è una tecnica di controllo della congestione utilizzata in diverse tecnologie di rete per **gestire** il flusso di dati in modo da evitare il **sovraccarico** della rete e garantire una trasmissione efficiente dei dati

---

Ad ogni [[Round Trip Time|RTT]] la dimensione della [[Finestra di congestione|CWND]] viene **incrementata** di `1` (*additive increase*)

Nel caso in cui si verifichi un [[Retransmission TimeOut|RTO]]:
1. L'**SSTHRESH** diventa la metà della CWND
2. La dimensione della **CWND** viene reimpostata ad `1`
3. Si ricomincia dalla fase di [[Slow Start]]

Nel caso in cui vengano ricevuti 3 **ACK duplicati**:
1. L'**SSTHRESH** diventa la metà della CWND
2. La dimensione della **CWND** si dimezza (*multiplicative decrease*)
3. Si ricomincia dalla fase di [[Congestion Avoidance]]