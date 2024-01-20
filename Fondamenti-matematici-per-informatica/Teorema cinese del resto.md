---
Created: 2022-04-19 16:01
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-matematici-per-informatica
---

Siano $n, m > 0$ e siano $a, b \in \mathbb{Z}$.
Consideriamo:
$$\begin{cases} x \in \mathbb{Z}\\ x \equiv a\ (mod\ n)\\ x \equiv b\ (mod\ m) \end{cases}$$
Sia $S := \{ x \in \mathbb{Z}\ |\ x \equiv a\ (mod\ n), x \equiv b\ (mod\ n) \}$ l'[[Analisi/Insiemi/Insieme|insieme]] delle soluzioni del sistema di congruenze precedenti.
Allora il sistema è **compatibile** ovvero $S \ne \emptyset$.

---

Inoltre se $S \ne \emptyset$ e $c \in S$ allora $\Rightarrow S = [c]_{[n, m]} = \{ c + k_{[n, m]} \in \mathbb{Z}\ |\ k \in \mathbb{Z} \}$.
