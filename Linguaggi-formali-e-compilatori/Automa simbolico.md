---
 Created: 2023-12-31 15:10
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Un **automa simbolico** è un particolare tipo di [[Automata|automa]], utilizzato principalmente nella [[Grammatica LALR(1)|grammatica LALR(1)]], che utilizza dei **simboli** (delle [[Variabile|variabili]]) al posto dei *lookahead set*

---

Gli **item** dell'automa simbolico sono formati da:
- Una componente di tipo [[Grammatica LR(0)|LR(0)]]
- Una parte composta da un insieme di *lookahead* simbolico

## Costruzione dell'automa simbolico

Nello [[Stato|stato]] iniziale dell'automa, si inserisce al posto del `$` una variabile $x_{0}$
La corrispondenza tra $x_{0}$ e `$` viene salvata in un **sistema di equazioni**

Per ogni nuovo stato si sostituiscono i *lookahead set*, prima di calcolare la chiusura, con delle nuove variabili e se ne tiene traccia nel sistema, se incontro una transizione ad uno stato già esistente, aggiorno la variabile nel sistema con la variabile presente nel *lookahead set* dello transizione

Infine si calcola la soluzione per il sistema di equazioni e si controllano che non vi siano conflitti
