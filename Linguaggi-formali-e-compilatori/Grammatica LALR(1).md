---
 Created: 2023-12-31 13:45
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **grammatica LALR(1)** è un tipo di [[Grammatica libera|grammatica libera]] utilizzato per rendere più efficiente il [[Bottom-Up parsing|parsing bottom-up]]

---

## Costruzione dell'automa caratteristico LRm(1)

L'[[Automata|automa]] LRm(1) $\mathcal{AM}$ è costruito a partire dall'[[Grammatica LR(1)#Costruzione dell'automa caratteristico|automa LR(1)]] $\mathcal{A}$ (la lettera $\mathcal{M}$ sta per *merged*)

Gli [[Stato|stati]] del nuovo automa sono ottenuti **unendo** all'interno di un singolo stato tutti gli item negli stati $\langle P_{1}, ..., P_{n} \rangle$ di $\mathcal{A}$ che hanno le stesse [[Grammatica LR(0)|LR(0)-proiezioni]], ossia con lo stesso item LR(0)
Se lo stesso stato $P$ in $\mathcal{A}$ ha la stessa $Y$-transizione a $Q$ e se $P$ è stato unito in $\langle P_{1}, ..., P_{n} \rangle$ e $Q$ in $\langle Q_{1}, ..., Q_{m} \rangle$, allora c'è una $Y$-transizione in $\mathcal{AM}$ da $\langle P_{1}, ..., P_{n} \rangle$ a $\langle Q_{1}, ..., Q_{m} \rangle$

Eseguendo l'operazione descritta il numero di stati dell'automa LRm(1) così generato sarà sicuramente uguale a quello dell'automa LR(0) con le stesse transizioni

## Costruzione della tabella di parsing

Le [[Tabella di parsing bottom-up|tabelle di parsing]] LALR(1) sono ottenute prendendo:
- L'automa caratteristico LRm(1)
- La *lookahead function* $\mathcal{LA}(P, A \rightarrow \beta) = \bigcup_{[A \rightarrow \beta \cdot, \Delta_{j}]} \Delta_{j}$
