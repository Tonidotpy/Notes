---
 Created: 2023-12-29 16:56
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Un **reducing item** è uno stato di un [[Automata|automa]] caratteristico di una [[Grammatica libera|grammatica]] che contiene una [[Produzione|produzione]] nella forma:
$$A \rightarrow \beta \cdot, \Delta$$
in cui il $\Delta$ specifica una condizione per cui l'analisi della produzione termina

---

Nel caso delle [[Grammatica LR(0)|grammatiche LR(0)]] il $\Delta$ è vuoto e di conseguenza l'item prende la forma di $A \rightarrow \beta \cdot$
