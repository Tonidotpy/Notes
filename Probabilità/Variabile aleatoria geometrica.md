---
 Created: 2022-05-03 10:07
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Variabile aleatoria geometrica
$$P_{X}(x) = \begin{cases} p(1 - p)^{x - 1}\ \ \ \ x \in \mathbb{N}\\ 0\ \ \ \ altrimenti \end{cases}$$
$$F_{X}(x) = P(X \le x) = \sum\limits_{t = 1}^{[x]}P(X = t) = \begin{cases} 1 - (1 - p)^{[x]}\ \ \ \ x \le 1\\ 0\ \ \ \ x > 1 \end{cases} $$

*Teorema*: $X_{1}, ..., X_{n} \sim Ber(p)$ tra loro [[Indipendenza stocastica|stocasticamente indipendenti]] allora:
$$X = \sum\limits_{i = 1}^{n} X_{i} \sim Bin(n, p)$$