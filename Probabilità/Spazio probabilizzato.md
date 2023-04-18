---
 Created: 2022-03-08 08:43
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Spazio di Kolmogorov]
 Tags: []
---

# Spazio probabilizzato

Dato uno [[Spazio probabilizzabile|spazio probabilizzabile]] ($\Omega, A$) una [[Probabilità|probabilità]] $P_r$ è una applicazione $P_r: A \mapsto \mathbb{R}^+$ tale che:
1. (**non negatività**) se $a \in A$ allora $P_r(A) \ge 0$;
2. (**normalizzazione**) $P_r(\Omega) = 1$;
3. (**$\sigma$ additività ** ) Se $\{ a_i \}_{i=1}^\infty\ |\ a_i \in A$ e a due a due disgiunti
  $a_i \cap a_j = \emptyset\ \forall i, j\ i \neq j$ allora:
  $$P_r(\bigcup_{i=1}^\infty a_i) = \sum_{i=1}^\infty P_r(a_i)$$
4. (**additività**) Se $\{ a_i \}_{i=1}^n\ |\ a_i \in A, a_i \cap a_j = \emptyset\ \forall i, j\ i \neq j$ allora:
  $$P_r(\bigcup_{i=1}^n a_i) = \sum_{i=1}^n P_r(a_i)$$
---

Dato uno [[Spazio campionario|spazio campionario]] $\Omega$, una [[Tribù|tribù]] $A$ di $\Omega$ e una [[Probabilità|probabilità]] $P_r$ sullo [[Spazio probabilizzabile|spazio probabilizzabile]] ($\Omega, A$) chiameremo la terna ($\Omega, A, P_r$) uno **spazio probabilizzato**.