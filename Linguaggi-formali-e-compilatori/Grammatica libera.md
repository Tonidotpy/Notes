---
 Created: 2023-09-15 09:07
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Una **grammatica libera** (o *context-free grammar*) è un tipo di [[Grammatica generativa|grammatica]] le cui [[Produzione|produzioni]] sono tutte nella forma $A \rightarrow \beta$, ovvero che hanno driver composti **solamente** da [[Simbolo|non terminali]]

---

Si dice che un [[Linguaggio|linguaggio]] è *context-free* se esiste una grammatica libera che genera quello stesso linguaggio:
$$\mathcal{L} = \mathcal{L}(\mathcal{G})$$

Le grammatiche libere si prestano in modo naturale ad essere processate tramite il cosiddetto [[Albero di derivazione|albero di derivazione]]

Dato un linguaggio context-free esiste una grammatica libera $\mathcal{G}$ tale che $\mathcal{L}(\mathcal{G}) = \mathcal{L}\ \backslash \{ \epsilon \}$ e **non** ha:
- [[Produzione epsilon|produzioni epsilon]]
- [[Produzione unitaria|produzione unitaria]]
- [[Simbolo|Non terminali inutili]], ossia che non appaiono in nessuna [[Derivazione|derivazione]]

## Proprietà di chiusura

### Unione

La classe dei linguaggi liberi è **chiusa** rispetto all'operazione di [[Unione|unione]] d'[[Insiemi|insiemi]]
$$\text{Se } \mathcal{L_{1}} \text{ è  libero } \land \mathcal{L_{2}} \text{ è libero} \Rightarrow \mathcal{L_{1}} \cup \mathcal{L_{2}} \text{ è libero}$$
Per unire due linguaggi liberi è necessario modificare i simboli non terminali evitano possibili collisioni e aggiungendo un nuovo *start-symbol* la cui produzione sono gli start-symbol dei due linguaggi

### Concatenazione

La classe dei linguaggi liberi è **chiusa** rispetto all'operazione di [[Concatenazione|concatenazione]]
$$\text{Se } \mathcal{L_{1}} \text{ è libero } \land \mathcal{L_{2}} \text{ è libero} \Rightarrow \{ \omega_{1} \omega_{2}\ |\ \omega_{1} \in \mathcal{L_{1} \land \omega_{2} \in \mathcal{L_{2}}} \}$$
Per concatenare due linguaggi liberi il procedimento è equivalente a quello dell'unione

### Intersezione

La classe dei linguaggi liberi è **chiusa** rispetto all'operazione di [[Intersezione|intersezione]]
$$\text{Se } \mathcal{L}_{1} \text{ è libero } \land \mathcal{L}_{2} \text{ è libero } \Rightarrow \mathcal{L}_{1} \cap \mathcal{L}_{2} \text{ è libero}$$