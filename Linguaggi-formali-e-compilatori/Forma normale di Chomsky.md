---
Created: 2023-09-22 09:03
Author: Antonio Gelain
aliases:
  - CNF
tags:
  - linguaggi-formali-e-compilatori
---

La **forma normale di Chomsky** è una [[Grammatica libera|grammatica libera]] con le seguenti proprietà:
- Non ha alcuna [[Produzione epsilon|produzione epsilon]], eccetto $S \mapsto \epsilon$
- Tutte le sue [[Produzione|produzioni]] hanno una delle seguenti forme:
    - $A \mapsto a$
    - $A \mapsto BC$, in cui sia $B$ sia $C$ sono diversi da $S$

---

> [!INFO] Data una grammatica libera $\mathcal{G}$, esiste **sempre** una grammatica in *CNF* $\mathcal{G}'$ tale che $\mathcal{L(G) = L(G')}$

Le grammatiche regolari in *CNF* sono più sintetiche e generano [[Linguaggio|linguaggi]] equivalenti a livello espressivo ma più puliti

## Eliminare le *epsilon produzioni*

Per eliminare le epsilon produzioni da una grammatica libera, basta eseguire un semplice procedimento ricorsivo:
1. **Caso base**: se la grammatica comprende una produzione nella forma $A \rightarrow \epsilon$, allora il [[Simbolo|non-terminale]] $A$ è annullabile
2. **Passo induttivo**: se la grammatica comprende una produzione nella forma $A \rightarrow Y_{1}Y_{2}...Y_{n}$ e i non-terminali $Y_{1}Y_{2}...Y_{n}$ sono tutti annullabili allora anche $A$ è annullabile