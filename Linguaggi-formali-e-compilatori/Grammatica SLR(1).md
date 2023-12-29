---
Created: 2023-12-29 17:25
Author: Antonio Gelain
aliases:
  - Grammatica Simple Left Rightmost(1)
tags:
  - linguaggi-formali-e-compilatori
---

 Una **grammatica SLR(1)** è un tipo di [[Grammatica libera|grammatica libera]] utilizzato per rendere più efficiente il [[Bottom-Up parsing|parsing bottom-up]]

---

## Costruzione della tabella di parsing

Una [[Tabella di parsing|tabella di parsing]] per la grammatica SLR(1) contiene informazioni grossolane, e questo è dovuto a due motivi:
1. Lo loro costruzione ha come base di partenza un [[Automata|automa]] caratteristico con [[Grammatica LR(0)|LR(0)-items]]
2. La funzione di *lookahead* è pari a $\mathcal{LA}(P, A \rightarrow \beta) = follow(A)$ per ogni $A \rightarrow \beta \cdot \in P$
