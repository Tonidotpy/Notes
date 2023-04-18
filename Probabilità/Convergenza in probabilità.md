---
 Created: 2022-05-17 09:30
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Convergenza in probabilità
La [[Successione di variabili aleatorie|successione di variabile aleatoria]] $\{ X_{i} \}^{\infty}_{i=1}$ **converge in probabilità** alla [[Variabili aleatorie|variabile aleatoria]] limite $X$ se $\forall \epsilon > 0$ la [[Successioni|successione numerica]]  definita tramite gli eventi $A_{i}$:
$$A_{i}= \{ \omega \in \Omega\ |\ X_{i}(\omega) - X(\omega) \ge \epsilon \}$$
$$a_{i} = P(A_{i})$$
converge a zero, cioè $\lim_{i \to \infty} a_{i} = 0$.
*Teorema:* Se la [[Successioni|successione]] $\{ X_{i} \}^{\infty}_{i=1}$ converge in [[Convergenza in media quadratica|media quadratica]] a $X$ allora la [[Successioni|succesione]] [[Convergenza in probabilità|converge in probabilità]] alla stessa [[Variabili aleatorie|variabile aleatoria]] limite.