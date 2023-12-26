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

---

## Proprietà di chiusura

### Unione

La classe di linguaggi regolari è **chiusa** rispetto all'[[Unione|unione]] 
$$\text{Se } \mathcal{L_{1}} \text{ è  regolare } \land \mathcal{L_{2}} \text{ è regolare } \Rightarrow \mathcal{L_{1}} \cup \mathcal{L_{2}} \text{ è regolare}$$
Essendo che i linguaggi sono regolari è possibile costruire un [[Automa a Stati Finiti Deterministico|DFA]] sia per $\mathcal{L}_{1}$ sia per $\mathcal{L}_{2}$; se a questo punto si prendono i due [[Automata|automi]] e li si lega tramite una [[Epsilon transizione|epsilon transizione]], per l'operazione di [[Espressione regolare#^99a71b|alternanza]] si ottiene nuovamente un linguaggio regolare

### Concatenazione

La classe di linguaggi regolari è **chiusa** rispetto alla [[Concatenazione|concatenazione]]
$$\text{Se } \mathcal{L_{1}} \text{ è regolare } \land \mathcal{L_{2}} \text{ è regolare} \Rightarrow \{ \omega_{1} \omega_{2}\ |\ \omega_{1} \in \mathcal{L_{1} \land \omega_{2} \in \mathcal{L_{2}}} \}$$
Anche per la concatenazione è possibile utilizzare la [[Costruzione di Thompson|costruzione di Thompson]] per ottenere un nuovo DFA che rappresenta la concatenazione dei due linguaggi regolari anch'esso regolare

### Complementazione

La classe di linguaggi regolari è **chiusa** rispetto alla [[Insiemi complementari|complementazione]]
$$\text{Se } \mathcal{L} \text{ è regolare con } \mathcal{A} \text{ alfabeto di } \mathcal{L} \Rightarrow \mathcal{A \backslash L} \text{ è regolare}$$
Per ottenere l'automa che denota il complementare di un linguaggio regolare basta rendere finali tutti gli stati che non lo sono e viceversa (questo funziona **solamente** se il DFA presenta una funzione di **transizione totale**)

### Intersezione

La classe di linguaggi regolari è **chiusa** rispetto all'[[Intersezione|intersezione]]
$$\text{Se } \mathcal{L_{1}} \text{ è  regolare } \land \mathcal{L_{2}} \text{ è regolare } \Rightarrow \mathcal{L_{1}} \cap \mathcal{L_{2}} \text{ è regolare}$$
Questa affermazione è derivabile dalla chiusura sull'unione utilizzando le regole di [[Leggi di De Morgan|De Morgan]]:
$$\mathcal{L}_{1} \cap \mathcal{L}_{2} = \lnot(\lnot(\mathcal{L}_{1} \cap \mathcal{L}_{2})) = \lnot(\lnot\mathcal{L}_{1} \cup \lnot\mathcal{L}_{2})$$
