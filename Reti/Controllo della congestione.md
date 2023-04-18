---
 Created: 2022-12-22 17:57
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **controllo della congestione** è un meccanismo utilizzato in diverse tecnologie di rete per **gestire il flusso** di dati in modo da evitare il **sovraccarico** della rete e garantire una trasmissione efficiente dei dati

---

Una congestione si manifesta attraverso la **perdita di pacchetti** e/o tramite dei **ritardi** più lunghi del normale

Una congestione avviene principalmente in 3 casi:
- Quando ci sono **ritardi elevati** a causa dell'alta frequenza di trasmissione rispetto a quella di ricezione
- Quando l'[[Retransmission TimeOut|RTO]] non è ottimale e vengono ritrasmessi troppi paccheti oppure vengono trasmessi ad una frequenza minore di quella ottimale
- Quando dei pacchetti vengono scartati a causa della congestione stessa

Esistono diversi **algoritmi** in TCP per gestire la congestione:
- [[Convex hUll-Based Internet Congestion control|CUBIC]]
- [[Bottleneck Bandwith and Round-trip propagation time|BBR]]

---

Esistono diverse tecniche che permettono il controllo della congestione *loss-based*, tra le quali:
- [[Additive Increase Multiplicative Decrease|AIMD]]
- [[Slow Start]]
- [[Congestion Avoidance]]
- [[Fast Retransmit]]
- [[Fast Recovery]]