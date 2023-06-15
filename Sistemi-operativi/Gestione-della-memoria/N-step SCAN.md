---
 Created: 2023-06-15 14:51
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria,algoritmo]
---

L'[[Algoritmo|algoritmo]] **N-step SCAN** è una variante dello [[SCAN]] che utilizza $n$ [[Coda|code]] di richieste per gestire l'accesso al [[Disco rigido|disco fisso]]

---

La coda delle richieste viene partizionata in $n$ code di dimensione massima $M$

Mentre una coda viene processata, gli accessi in arrivo riempiono le altre code
Una volta che una coda è piena è pronta per essere processata

Se la $M$ scelta è troppo grande l'algoritmo degenera in uno SCAN, mentre se è pari a 1, degenera in [[First Come First Served|FCFS]]

La variante con due sole code viene chiamata **FSCAN**