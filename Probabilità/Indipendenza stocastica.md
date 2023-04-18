---
 Created: 2022-03-30 14:30
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Indipendenza stocastica

Dati due [[Esito|eventi]] $A$ e $B$ sono **stocasticamente indipendenti** se:
> $$P(A \cap B) = P(A)P(B)$$

Dati $n$ eventi sono **stocasticamente indipendenti** se:
> $$P(\bigcap_{i=1}^{k}A_{i})= \prod_{i=1}^{k} A_{i}$$

---

- $P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(A)P(B)}{P(B)} = P(A)\ \ \ \ P(B) > 0$

Se due [[Esito|eventi]] sono tra loro **incompatibili** allora **non** sono **stocasticamente indipendenti**:
$$0 = P(\emptyset) = P(A \cap B) \ne P(A)P(B) > 0$$
Due [[Variabili aleatorie|variabili aleatorie]] $(X, Y)$ discrete sono tra loro **stocasticamente indipendenti** se:
$$p_{X, Y}(x, y) = p_{X}(x)p_{Y}(y)\ \ \ \ \forall (x, y) \in R_{X} \times R_{Y}$$
Se due [[Variabili aleatorie|variabili aleatorie]] $(X, Y)$ sono **stocasticamente indipendenti** allora:
$$p_{X|Y}(x|y) = p_{X}(x)$$
$$p_{Y|X}(y|x) = p_{Y}(y)$$
