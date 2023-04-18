---
 Created: 2022-05-03 10:06
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Variabile aleatoria binomiale
$$P(B) = p^{x} (1 - p)^{n - x}$$
$$P(X = x) = {n \choose x} p^{x}(1 - p)^{n - x}$$
### Proprietà
Si può approssimare la **distribuzione  binomiale** con la [[Variabile aleatoria normale|distribuzione normale]].
$${X_{i}}^{\infty}_{i=1}, X_{i} \sim Ber(p)$$
$$n\overline{X}_{n} = \sum\limits_{i=1}^{n} X_{i} \sim Bin(n, p)\ \ \ \ E(n\overline{X}_{n}) = np\ \ \ \ Var(n\overline{X}_{n}) = p(1 - p) \cdot n$$
Dal [[Teorema centrale del limite|teorema centrale del limite]] abbiamo che:
$$\overline{X}_{n} \sim N(p, \frac{p(1 - p)}{n})$$
allora
$$n\overline{X}_{n} = \sum\limits^{n}_{i=1} X_{i} = N(np, np(1 - p))$$
L'approssimazione è "*buona*" quando:
- $n$ è abbastanza grande;
- $p$ e $(1 - p)$ sono lontani da 0.
Regola del pollice:
- si calcola l'intervallo $np \pm 3\sqrt{np(1 - p)}$;
- l'approsimazione è buona se l'intervallo è contenuto nell'intervallo $[0, n]$.