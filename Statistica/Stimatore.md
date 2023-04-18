---
 Created: 2022-05-24 09:18
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Stimatore


### Proprietà
###### Errore quadratico medio
Supponiamo di utilizzare uno **stimatore** $T = T(X_{1}, ..., X_{n})$ per la quantità ignota $\mu$ allora:
$$MSE(T,\mu)= E[(T - \mu)^{2}] = Var(T) + (E(T) - \mu)^{2}$$
###### Distorsione dello stimatore
$$B(T, \mu) = E(T) - \mu= E(T - \mu)$$
Diremo che uno **stimatore** è **non** distorto se $B(T, \mu) = 0\ \ \ \ \forall n$.
Uno **stimatore** è non distorto asintoticamente se $\lim_{n \to \infty} B(T, \mu) = 0$.
$\lim_{n \to \infty} MSE(T, \mu) = 0$ quando ciò accade, allora la successione degli **stimatori** indicizzati tramite la dimensione del campione $T_{1}, T_{2}, ... \Rightarrow (T_{n})^{\infty}_{n=1}$ [[Convergenza in media quadratica|converge in media quadratica]] a $\mu$.
Diremo che lo **stimatore** è consistente in media quadratica.
$Var(T)$: efficiente
$$\lim_{n \to \infty} MSE(T, \mu) = \begin{cases} \lim_{n \to \infty} Var(T) = 0 \\
\lim_{n \to \infty} B(T) = 0 \end{cases}$$