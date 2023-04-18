---
 Created: 2022-05-10 21:24
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Valore atteso condizionato
Valore atteso condizionato della **variabile aleatoria** $X$ data la **variabile aleatoria** $Y$ nel caso **discreto**:
$$E(X|Y = y) = \sum\limits_{x \in R_{X}} x p_{X|Y} (x|y)$$
###### Momenti condizionati non centrati
$$E(X^{n}|Y = y) = \sum\limits_{x \in R_{X}} x^{n} p_{X|Y}(x|y)\ \ \ \ \forall n \in \mathbb{N}$$
[[Varianza]] condizionata della **variabile aleatoria** $X$ data la **variabile aleatoria** $Y$ nel caso **discreto**:
$$Var(X|Y = y) = E((X - E(X|Y = y))^{2}|Y = y) = \sum\limits_{x \in R_{X}} (x - E(X|Y = y))^{2} p_{X|Y}(x|y)$$