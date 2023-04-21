---
 Created: 2022-12-23 16:17
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [CUBIC]
 Tags: [algoritmo]
---

L'algoritmo **Convex hUll-Based Internet Congestion control** (*CUBIC*) è una tecnica di **controllo** della congestione utilizzata in diverse tecnologie di rete per **gestire** il flusso di dati in modo da **evitare** il sovraccarico della rete e garantire una trasmissione efficiente dei dati

---

Per un migliore utilizzo e stabilità della rete, CUBIC usa entrambi i profili, concavo e convesso, di una **funzione cubica** per aumentare la dimensione della [[Finestra di congestione|finestra di congestione]]
$$\text{CWDN}_{\text{cubic}}(t) = C(t - K)^{3} + \text{CWDN}_{\text{max}}$$
Dove:
- $K = \sqrt[3]{\frac{\text{CWND}_\text{max} (1 - \beta)}{C}}$
- $C = 0.4$
- $\beta = 0.7$

In questo modo CUBIC bilancia **scalabilità** e **velocità** di convergenza