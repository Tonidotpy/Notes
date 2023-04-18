---
 Created: 2022-05-04 15:19
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Indipendenza in media

Date due [[Variabili aleatorie|varaibili aleatorie]] $(X, Y)$ diremo che $X$ è **indipendente in media** da $Y$ se:
$$E(X|Y = y) = E(X)\ \ \ \ \forall y \in R_{Y}$$
*Teorema*: Se $X$ e $Y$ sono [[Indipendenza stocastica|stocasticamente indipendenti]] allora sonotra loro **indipendenti in media**:
$$E(X|Y = y) = \sum\limits_{x \in R_{X}} x p_{X|Y}(x|y) = \sum\limits_{x \in R_{X}} x p_X(x) = E(X)$$
### Indice di indipendenza in media (rapporto di correlazione)
$$0 \le \eta^{2}_{X|Y} = \frac{Var(E(X|Y))}{Var(X)} = 1 - \frac{E(Var(X|Y))}{Var(X)} \le 1\ \ \ \ \text{se } Var(x) > 0$$

### Proprietà
- Se $\eta^{2}_{X|Y} = 0$ allora $X$ è **indipendente in media** da $Y$;
- Se $\eta^{2}_{X|Y} > 0$ allora $X$ è **dipendente in media** da $Y$;
- Se $\eta^{2}_{X|Y} = 1$ se e solo se $P(X = E(X|Y)) = 1$
La [[Variabili aleatorie|variabile aleatoria]] $X$ è **indipendente in varianza** da $Y$ se:
$$Var(X|Y = y) = \sigma^{2}\ \ \ \ \forall y \in R_Y$$
###### Momenti misti di ordine $r$ e $s$
$$E(X^{r} Y^{s}) = \sum\limits_{X \in R_{X}} \sum\limits_{y \in R_{Y}} x^{r} y^{s} p_{X, Y}(x, y)$$
$$E((X  E(X)^{r}(Y E(Y)^{s}))$$
...
// TODO: 