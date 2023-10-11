---
Created: 2023-10-05 11:22
Author: Antonio Gelain
aliases: 
tags:
---

Sia ($S, \mathcal{A}, \text{move}_{n}, S_{0}, F$) un [[Automa a Stati Finiti Non-deterministico|NFA]], sia $t$ uno stato in $S$ e $T$ un [[Sottoinsieme|sottoinsieme]] di $S$.
Definiamo **$\epsilon$-chiusura**($\{ t \}$) l'insieme di stati in $S$ che sono raggiungibili da $t$ tramite zero o più **$\epsilon$-transizioni**
$$\epsilon\text{-chiusura}(T) = \bigcup_{t \in T} \epsilon\text{-chiusura}(\{ t \})$$

---

In una simulazione di NFA la $\epsilon$-chiusura ci permette di ricavare gli stati successivi che posso raggiungere dal nodo corrente dell'iterazione successiva

Si può definire la $\epsilon$-chiusura($M$), dato $N = (S, \mathcal{A}, \text{move}_{n}, S_{0}, F)$ un NFA e $M \subseteq S$, come il **più piccolo** insieme di $X \subseteq S$ tale che $X$ è una soluzione alla seguente equazione:
$$X = M \cup \{ N'\ |\ N \in X \cap N' \in \text{move}_{n}(N, \epsilon) \}$$

Si può notare come la definizione di $X$ dipenda da $X$ stessa, per questo è importante notare che si prende il più piccolo insieme in modo da evitare [[Ciclo|cicli]] infiniti
A questo proposito entra in gioco il [[Teorema del punto fisso|teorema del punto fisso]]