---
 Created: 2022-04-19 16:01
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Teorema cinese del resto
Siano $n, m > 0$ e siano $a, b \in \mathbb{Z}$.
Consideriamo:
$$\begin{cases} x \in \mathbb{Z}\\ x \equiv a\ (mod\ n)\\ x \equiv b\ (mod\ m) \end{cases}$$
Sia $S := \{ x \in \mathbb{Z}\ |\ x \equiv a\ (mod\ n), x \equiv b\ (mod\ n) \}$ l'[[Insiemi|insieme]] delle soluzioni del sistema di congruenze precedenti.
Allora il sistema è **compatibile** ovvero $S \ne \emptyset$.
Inoltre se $S \ne \emptyset$ e $c \in S$ allora $\Rightarrow S = [c]_{[n, m]} = \{ c + k_{[n, m]} \in \mathbb{Z}\ |\ k \in \mathbb{Z} \}$.