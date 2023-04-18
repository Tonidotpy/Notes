---
 Created: 2022-03-09 13:58
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Costruzione di una probabilità

> Definiamo **costruzione di una probabilità** in uno [[Spazio probabilizzabile|spazio probabilizzabile]] dove $\Omega$ è al più numerabile come $\Omega = \{ \omega_1, \omega_2, ... \} = \{ \omega_i \}_{i=1}^\infty$.
> Ad ogni $\omega_i \in \Omega$ assegniamo un peso $p(\{ \omega_i \})\ i=1, ...$
> 1. $p(\{ \omega_i \}) \ge 0$;
> 2. $\sum_{i=1}^\infty p(\{ \omega_i \}) = 1$.

---

La [[Probabilità|probabilità]] di un [[Esito|evento]] $A$ è data da:
$$P_r(A) = P_r(\bigcup_{\omega_i \in A} \{ \omega_i \}) = \sum_{\omega_i \in A} P_r(\{ \omega_i \}) = \sum_{\omega_i \in A} p(\{ \omega_i \})$$
$\Omega = \bigcup_{i = 1}^\infty \omega_i$     $P_r(\Omega) = \sum_{i = 1}^\infty P_r(\{ \omega_i \}) = \sum_{i=1}^\infty p = \infty$.

Quindi è impossibile che i pesi abbiano tutti lo stesso valore?

