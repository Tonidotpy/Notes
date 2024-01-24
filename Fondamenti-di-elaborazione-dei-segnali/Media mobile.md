---
 Created: 2024-01-24 10:27
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **media mobile** è un [[Analisi/Insiemi/Insieme|insieme]] di dati che consiste nel creare una [[Serie|serie]] di [[Media|medie]] di vari [[Sottoinsieme|sottoinsiemi]] dell'[[Analisi/Insiemi/Insieme|insieme]] completo

---

>[!INFO] Maggiore è la grandezza del kernel maggiore sarà l'attenuazione del segnale filtrato che avrà quindi [[Frequenza di un segnale|frequenza]] minore

Il **kernel** di un [[Filtro passa-basso|filtro]] che utilizza la media mobile presenta coefficienti il cui valore è sempre lo stesso
$$h[k] = \begin{bmatrix} \frac{1}{K} & ... & \frac{1}{K} \end{bmatrix} = \frac{1}{K} \begin{bmatrix} 1 & ... & 1\end{bmatrix}$$
