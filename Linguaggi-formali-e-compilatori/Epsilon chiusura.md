---
 Created: 2023-10-05 11:22
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Sia ($S, \mathcal{A}, \text{move}_{n}, S_{0}, F$) un [[Automa a Stati Finiti Non-deterministico|NFA]], sia $t$ uno stato in $S$ e $T$ un sottoinsieme di $S$.
Definiamo **$\epsilon$-chiusura**($\{ t \}$) l'insieme di stati in $S$ che sono raggiungibili da $t$ tramite zero o più **$\epsilon$-transizioni**
$$\epsilon\text{-chiusura}(T) = \bigcup_{t \in T} \epsilon\text{-chiusura}(\{ t \})$$

---

