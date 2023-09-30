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

Per dimostrare che un linguaggio non è libero utilizzando il *pumping lemma* per contraddizione bisogna seguire i seguenti step:
1. Si assuma che $\mathcal{L}$ è un linguaggio libero ^b0c485
2. $\mathcal{L}$ ha una **lunghezza di pumping** $P$
3. Tutte le stringhe più lunghe di $P$ possono essere *"pumped"*
4. Si trovi una stringa $z \in \mathcal{L}$ tale che $|z| \ge P$
5. Si divida $z$ in **5 parti** $uvwxy$
6. Si dimostri che $uv^{i}wx^{i}y \notin \mathcal{L}$ per qualche $i$
7. Si dimostri che la stessa cosa per tutte le possibili combinazioni di $uvwxy$ data la stessa $i$
8. $z$ non può essere *"pumped"* il che è una **contraddizione** col punto [[Pumping lemma#^b0c485|[1]]]