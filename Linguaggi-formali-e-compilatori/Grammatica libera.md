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

Se due linguaggi $\mathcal{L_{1}}$ e $\mathcal{L}_{2}$ sono linguaggi liberi allora la loro [[Unione|unione]] genera un linguaggio libero.