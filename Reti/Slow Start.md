---
 Created: 2022-12-23 15:27
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Lo **Slow Start** è una tecnica di controllo di flusso utilizzata in diverse tecnologie di rete per **gestire** il flusso di dati tra due punti di una rete e **garantire** una trasmissione efficiente dei dati

---

La dimensione della [[Finestra di congestione|finestra di congestione]] (*CWND*) viene **raddoppiata** ad ogni [[Round Trip Time|RTT]] **incrementandone** la grandezza di `1` ad ogni ACK ricevuto

Valogono le regole di [[Additive Increase Multiplicative Decrease|AIMD]] per il **rilevamento della congestione**