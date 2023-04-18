---
 Created: 2022-03-29 15:42
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Massimo Comune Divisore
Siano $n, m \in \mathbb{Z} \backslash \{ 0 \}$.
Diciamo che $d \in \mathbb{N}$ è un **massimo comune divisore** (o *MCD*) tra $n$ e $m$ se $d > 0$ e:
1. $\frac{n}{d}$ e $\frac{m}{d}$;
2. Se $c \in \mathbb{Z}$, $\frac{n}{c}$ e $\frac{m}{c}$ allora $\frac{d}{c}$.

Definiamo:
$$S := \{ s \in \mathbb{N}\ |\ s = xn + ym \text{ per qualche } x, y \in \mathbb{Z} \}$$
Grazie al [[Assioma del buon ordinamento|teorema del buon ordinamento]] abbiamo che $d := \min{(S)}$
Osserviamo $d \in S$, dunque esistono $x, y \in \mathbb{Z}$ tali che:
$$d = xn + ym > 0$$
