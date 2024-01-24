---
 Created: 2024-01-24 14:40
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Il **filtro mediano** è un particolare [[Filtro di rango|filtro di rango]] in cui viene sostituito il valore centrale della finestra col **valore centrale** nella finestra
$$a_{i} = \begin{cases}
0 & \forall i \ne \lfloor\frac{N}{2}\rfloor \\
1 & i = \lfloor\frac{N}{2}\rfloor
\end{cases}$$

---

