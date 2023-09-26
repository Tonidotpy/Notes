---
 Created: 2023-09-22 09:13
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **pumping lemma** riguarda la presenza in ogni [[Grammatica libera|linguaggio libero]] infinito di [[Successioni|successioni]] di stringhe che presentano regolarità ben definite.

---

>[!INFO] Il pumping lemma viene utilizzato per dimostrare che un linguaggio **non** è libero

Consideriamo un linguaggio libero $\mathcal{L}$, allora:
$$\exists p \in \mathbb{N}^{+}\ |\ \forall z \in \mathcal{L}\ :\ |z| > p \rightarrow \exists u, v, w, x, y\ |\ z = uvwxy \land |vwx| \le p \land |vx| > 0 \land \forall i \in \mathbb{N}.uv^{i}wx^{i}y \in \mathcal{L}$$
