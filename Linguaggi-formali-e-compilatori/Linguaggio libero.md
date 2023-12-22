---
Created: 2023-12-19 16:05
Author: Antonio Gelain
aliases:
  - Linguaggio context-free
tags:
  - linguaggi-formali-e-compilatori
---

Un **linguaggio libero** è un tipo di [[Linguaggio|linguaggio]] generato da una [[Grammatica libera|grammatica libera]]

---

## Proprietà di chiusura

### Unione

La classe dei linguaggi liberi è **chiusa** rispetto all'operazione di [[Unione|unione]] d'[[Analisi/Insiemi/Insieme|insiemi]]
$$\text{Se } \mathcal{L_{1}} \text{ è  libero } \land \mathcal{L_{2}} \text{ è libero} \Rightarrow \mathcal{L_{1}} \cup \mathcal{L_{2}} \text{ è libero}$$
Per unire due linguaggi liberi è necessario modificare i simboli non terminali evitando possibili collisioni e aggiungendo un nuovo *start-symbol* la cui produzioni sono gli *start-symbol* dei due linguaggi

### Concatenazione

La classe dei linguaggi liberi è **chiusa** rispetto all'operazione di [[Concatenazione|concatenazione]]
$$\text{Se } \mathcal{L_{1}} \text{ è libero } \land \mathcal{L_{2}} \text{ è libero} \Rightarrow \{ \omega_{1} \omega_{2}\ |\ \omega_{1} \in \mathcal{L_{1} \land \omega_{2} \in \mathcal{L_{2}}} \}$$
Per concatenare due linguaggi liberi il procedimento è equivalente a quello dell'unione, ad eccezione della produzione del nuovo *start-symbol* che può essere derivato nella concatenazione degli *start-symbol* dei due linguaggi invece che dall'unione

### Intersezione

La classe dei linguaggi liberi **NON è chiusa** rispetto all'operazione di [[Intersezione|intersezione]]

Si può dimostrare per contraddizione trovando anche un solo caso dove l'intersezione dei due linguaggi non è un linguaggio libero, ad esempio:
$$
\begin{matrix}
\mathcal{L}_{1} = \{ a^{n} b^{n} c^{j}\ |\ n, j > 0 \} \\
\mathcal{L}_{2} = \{ a^{j} b^{n} c^{n}\ |\ n, j > 0 \} \\
\mathcal{L}_{1} \cap \mathcal{L}_{2} = \{ a^{n} b^{n} c^{n}\ |\ n > 0 \}
\end{matrix}
$$