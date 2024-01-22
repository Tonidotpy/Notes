---
Created: 2024-01-22 13:33
Author: Antonio Gelain
aliases:
  - Iterazione di Voronoi
  - Rilassamento di Voronoi
tags:
  - fondamenti-di-elaborazione-dei-segnali
  - algoritmo
---

L'**algoritmo di Lloyd-Max** (o *iterazione di Voronoi*) è un [[Algoritmo|algoritmo]] utilizzato per trovare un [[Analisi/Insiemi/Insieme|insieme]] di [[Punto|punti]] equidistanti in [[Sottoinsieme|sottoinsiemi]] di [[Spazio euclideo|spazi euclidei]], e partizioni di questi sottoinsiemi in celle

---

I [[Dato|dati]] necessari per l'esecuzione dell'algoritmo sono:
- La conoscenza della [[Funzione di distribuzione|distribuzione]] del [[Segnale|segnale]] $f_{x}(x)$
- La scelta a priori del numero di livelli del [[Quantizzazione|quantizzatore]] $N$

L'algoritmo è il seguente:
1. Si scelgono arbitrariamente un set iniziale di livelli $a_{i} : 1 \le i \le N$ (es. partire da livelli uniformi)
2. Si impostano i **punti di soglia** $b_{j} : 1 \le j \le N-1$ ai valori centrali tra livelli successivi, ossia $b_{j} = \frac{1}{2}(a_{j+1} + a_{j})$ ^b6092b
3. Si ricalcolano i livelli di quantizzazione $a_{i}$ imponendo pari alla [[Media|media]] della differenza di potenza[^1] nella finestra ($b_{i-1}, b_{i}$), dove gli estremi $b_{0}$ e $b_{n}$ sono posti a $\mp \infty$ 
4. Si calcola l'[[Errore quadratico medio|errore quadratico medio]] e lo si confronta col passo precedente
5. Se la variazione è inferiore a una data soglia ci si ferma, altrimenti si ripete il procedimento dal [[#^b6092b|punto 2]]

[^1]: Sulle slide c'è scritto DDP ma non viene specificato di cosa si tratta