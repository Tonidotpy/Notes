---
 Created: 2022-03-10 10:13
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Ordinamento dei numeri naturali
Sia $X$ un [[Insiemi|insieme]] non vuoto e sia $R$ una relazione binaria se $X$ (cioé $R \subset X \times X$).
Si dice che $R$ è un **ordinamento parziale** di $X$ se:
1. $x R x\ \forall x \in X$ (**proprietà riflessiva**);
2. $(x R y)$ e $(y R x) \Rightarrow x = y$ (**proprietà antisimmetrica**);
3. $(x R y)$ e $(y R z) \Rightarrow x R z$ (**proprietà transitiva**);
   Se in aggiunta val la seguente **proprietà tricotomica** allora si dice che $R$ è un **ordine totale** di X.
4. $\forall x, y \in X$, $x R y$ vera oppure $y R x$.
   Usualmente si utilizza $R = \le$.
   Se $\le$ è un **ordinamento parziale** di $X_1 (X_1 \le)$ si dice **insieme parzialmente ordinato**.
   Se $\le$ è un **ordinamento totale** di $X_1 (X_1 \le)$ si dice **insieme totalmente ordinato**.

Per ogni $n, m \in \mathbb{N}$, poniamo $n \le m$ se $\exists k \in \mathbb{N}\ |\ m = n + k$