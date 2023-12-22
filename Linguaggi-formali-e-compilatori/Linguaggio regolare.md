---
 Created: 2023-12-22 21:32
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Un **linguaggio regolare** è un linguaggio generato da una [[Grammatica regolare|grammatica regolare]] e può essere **denotato** da un [[Espressione regolare|espressione regolare]]

---

Dato un [[Alfabeto|alfabeto]] $\mathcal{A}$, un linguaggio regolare denotato da un espressione $\mathcal{L}(r)$ e definibile tramite [[Principio di induzione|induzione]] nel seguente modo:
- **Passo base**:
    - $\mathcal{L}(a) = \{ a \}\ \forall a \in \mathcal{A}$
    - $\mathcal{L}(\epsilon) = \{ \epsilon \}$
- **Passo induttivo**:
    - Se $r = r_{1}\ |\ r_{2}$ allora $\mathcal{L}(r) = \mathcal{L}(r_{1}) \cup \mathcal{L}(r_{2})$
    - Se $r = r_{1} r_{2}$ allora $\mathcal{L}(r) = \{ w_{1}w_{2}\ |\ w_{1} \in \mathcal{L}(r_{1}) \land w_{2} \in \mathcal{L}(r_{2}) \}$
    - Se $r = r^{*}$ allora $\mathcal{L}(r) = \{ \epsilon \} \cup \{ w_{1}w_{2}...w_{k}\ |\ k \ge 1 \land \forall i : 1 \le i \le k.w_{i} \in \mathcal{L}(r_{1}) \}$
    - Se $r = (r_{1})$ allora $\mathcal{L}(r) = \mathcal{L}(r_{1})$

L'ordine di precedenza in assenza di parentesi è il seguente:
$$\text{Kleene Start} < \text{Concatenazione} < \text{Alternanza}$$

Perciò l'espressione $a\ |\ b c^{*}$ si tradurrebbe in $(a\ |\ (b (c^{*})))$
