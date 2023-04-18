---
 Created: 2022-05-03 15:35
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Crittografia RSA
###### Teorema fondamentale
$$MCD(c, \phi(n)) = 1$$


*Corollario*: Siano $n, a \in \mathbb{Z}$ tale che $n > 0, (a, n) = 1, c > 0$.
Consideriamo la seguente congruenza:
$$\begin{cases} x \in \mathbb{Z} \\
x^{c} \equiv a\ (mod\ n) \end{cases}$$
Consideriamo anche $S := \{ x \in \mathbb{Z}\ |\ x \text{ soddisfa il sistema} \}$.
Se $MCD(c, \phi(n)) = 1$ allora possiamo calcolare $d > 0\ |\ d \in [c]^{-1}_{\phi(n)}$ e vale :
$$S = [a^{d}]_{n} \subset \mathbb{Z} = \{ a^{d} + kn \in \mathbb{Z}\ |\ k \in \mathbb{Z} \}$$
