---
Created: 2023-10-24 22:55
Author: Antonio Gelain
aliases: 
tags:
  - logica-computazionale
---

Una **funzione di interpretazione** $\mathcal{I}_{\mathcal{A}}$ è definita come una [[Funzione|funzione]] il cui [[Dominio|dominio]] è un [[Teoria asserzionale|teoria asserzionale]] mentre il codominio è un [[Modello|modello]]:
$$\mathcal{I_{A} : T_{A}} \rightarrow M$$

---

Si dice perciò che un fatto $f \in M$ è un **interpretazione** di $a \in \mathcal{T_{A}}$
$$f = \mathcal{I_{A}}(a) = a^{\mathcal{I_{A}}}$$
Oppure che $a$ **denota** $f$

Se si ha la stessa interpretazione per più fatti diversi si ha un fenomeno di [[Polisemia|polisemia]]

Viceversa quando si hanno più interpretazioni per uno stesso fatto si ha una [[Sinonimia|sinonimia]]

Una funzione di interpretazione:
- Non permette la polisemia
- Non ammette sinonimia
- È totale, perciò qualsiasi elemento del linguaggio è definito nel suo dominio di riferimento
- Non è (necessariamente) **surgettiva**
- È **composizionale**, ossia il significato dell'[[Asserzione|asserzione]] è codificata all'interno della sua stessa struttura

---

La [[Rappresentazione intensiva|rappresentazione intensiva]] di una funzione di interpretazione definita come:
$$\mathcal{I_{A}}^{i} = \langle \mathcal{I_{e}}, \mathcal{I_{C}}, \mathcal{I_{P}} \rangle$$
con:
- Una **funzione di interpretazione delle [[Entità|entità]]** $\mathcal{I_{e}}\ :\ \mathcal{E} \mapsto E$
- Una **funzione di interpretazione dei concetti** $\mathcal{I_{C}}\ :\ \{ \mathcal{C} \} \mapsto \{ E \}$
- Una **funzione di interpretazione delle proprietà** $\mathcal{I_{P}}\ :\ \{ \mathcal{P}^{n} \} \mapsto \{ E \} \times ... \times \{ E \}$
