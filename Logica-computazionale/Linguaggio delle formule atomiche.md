---
Created: 2023-11-04 21:40
Author: Antonio Gelain
aliases: 
tags:
  - logica-computazionale
---

Una **linguaggio delle formule atomiche** è definito come l'[[Unione|unione]] tra un [[Linguaggio asserzionale|linguaggio delle asserzioni atomiche]] ed un [[Linguaggio delle asserzioni complesse|linguaggio delle asserzioni complesse]]
$$\mathcal{L_{a} = L_{A} \cup  L_{AC}}$$

---

La [[Rappresentazione intensiva|rappresentazione intensiva]] del linguaggio delle formule atomiche viene definita come:
$$\mathcal{L_{a}^{i}} = \langle A_{a}, \{ FR \}_{a} \rangle$$
dove:
- $A_{a}$ è un **alfabeto** di $\mathcal{L_{a}}$ definito come $A_{a} = \langle E, \{ C \}, \{ P \} \rangle$, con:
    - Un [[Analisi/Insiemi/Insieme|insieme]] di nomi di [[Entità|entità]] $E$
    - Un insieme di **concetti** $\{ C \}$
    - Un insieme di **proprietà** $\{ P \}$, dove una proprietà è il nome di una [[Relazione|relazione]]
- $\{ FR \}_{a}$ è un insieme di [[Regola di formazione|regole di formazione]]