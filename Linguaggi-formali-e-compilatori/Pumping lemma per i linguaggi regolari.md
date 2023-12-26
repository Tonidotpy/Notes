---
 Created: 2023-12-26 14:50
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Il **pumping lemma** riguarda la presenza in ogni [[Linguaggio regolare|linguaggio regolare]] infinito di [[Successioni|successioni]] di stringhe che presentano regolarità ben definite.

---

>[!INFO] Il pumping lemma viene utilizzato per dimostrare che un linguaggio **NON** è regolare

Consideriamo un linguaggio regolare $\mathcal{L}$, allora:
- $\exists p \in \mathbb{N}^{+}$ tale che
- $\forall z \in \mathcal{L}\ :\ |z| > p$, allora
- $\exists u, v, w$ tale che:
    - $z = uvw \land$
    - $|uv| \le p \land$
    - $|v| > 0 \land$
    - $\forall i \in \mathbb{N}.uv^{i}w \in \mathcal{L}$

## Dimostrazione

Dato che $\mathcal{L}$ è un linguaggio regolare, sappiamo che esiste un [[Automa a Stati Finiti Deterministico|DFA]] $\mathcal{D} = (S, \mathcal{A}, \text{move}_{d}, S_{0}, F)$ tale per cui $\mathcal{L = L(D)}$

Fissando quindi $p = |S| - 1$; vorremmo far notare che tutti i cammini che partono da $S_{0}$ ed arrivano ad uno stato finale, passando per ogni stato al massimo una volta hanno lunghezza limitata da $p$

Quindi se per una parola $z$ vale $|z| > p$, allora possiamo scomporre $z$ in $z = a_{1}...a_{p} z'$ e abbiamo la certezza che almeno uno stato, diciamo $s^{*}$, sia attraversato più di una volta lungo il cammino $a_{1} ... a_{p}$

Questo significa che esiste un [[Ciclo|ciclo]] in $\mathcal{D}$ che parte da $s^{*}$ e torna in $s^{*}$, e questo ciclo si può indicare come $a_{i+1} ... a_{j}$, con $i < j \le p$

Definiamo ora $u$, $v$ e $w$:
- $u = a_{1}...a_{i}$
- $v = a_{i+1}...a_{j}$ (quindi $v$ rappresenta il ciclo)
- $w = \begin{cases} z' & \text{se } j = p \\ a_{j+1}...a_{p}z' & \text{se } j < p\end{cases}$
Quindi possiamo tranquillamente affermare che $|uv| \le p$ e che la lunghezza di $v$ è almeno $1$ (per definizione di ciclo ha almeno un nodo)
Inoltre esseno $v$ il ciclo, esso è ripetibile(*pumping*) un numero indefinito di volte, con la garanzia che $uv^{i}w$ sia accettato da $\mathcal{D}$ per ogni valore $i \in \mathbb{N}$
