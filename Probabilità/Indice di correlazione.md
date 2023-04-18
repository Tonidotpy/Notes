---
 Created: 2022-05-11 13:55
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Indice di Pearson]
 Tags: []
---

# Indice di correlazione
$$\rho(aX + b, cY + d) = \frac{Cov(aX + b, cY + d)}{\sqrt{Var(aX + b) \cdot Var(cY + d)}} = \frac{ac}{\sqrt{a^{2}c^{2}}}\rho(X, Y) = sign(ac)\rho(X, Y)$$
Siano $X_{1}, ..., X_{n}$ delle [[Variabili aleatorie|variabili aleatorie]]
$$\mu_{i} = E(X_{i})\ \ \ \ \sigma_{ii} = Var(X_{i})\ \ \ \ \sigma_{ij} = Cov(X_{i}, X_{j})$$
$$X = \sum\limits_{i = 1}^{n} (aX_{i} + b)$$
$$E(X) = \sum\limits_{i=1}^{n} a_{i}E(X_{i}) + \sum\limits_{i=1}^{n} b_{i}$$
$$Var(X) = \sum\limits_{i=1}^{n} \sum\limits_{j=1}^{n} a_{i}a_{j} Cov(X_{i}, X_{j}) = \sum\limits_{i=1}^{n} \sum\limits_{j=1}^{n} a_{i}a_{j} \sigma_{ij}$$
Se $X$ e $Y$ sono **incorrelate**, cioè $\rho(X, Y) = 0$
$$Var(aX + bY + c) = a^{2}Var(X) + b^{2}Var(Y) + 2abCov(X, Y) = a^{2}Var(X) + b^{2}Var(Y)$$

Se $X_{i}$ sono tali che:
- $E(X_{i}) = \mu$;
- $Var(X_{i}) = \sigma^{2}$;
- $Cov(X_{i}, X_{j}) = 0$.
allora:
- $\overline{X} = \frac{1}{n}\sum\limits X_{i}$;
- $E(\overline{X}) = \mu$;
- $Var(\overline{X}) = \frac{\sigma^{2}}{n}$.