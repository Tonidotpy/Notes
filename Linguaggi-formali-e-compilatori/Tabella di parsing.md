---
 Created: 2023-12-29 16:41
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **tabella di parsing** è un particolare tipo di tabella che viene utilizzata dai [[Analisi sintattica|parser]] per analizzare diversi tipi di [[Grammatica libera|grammatiche]]

---

## Costruzione di una tabella di parsing

Dobbiamo costruire una tabella con delle *entries* di forma $M[P, Y]$, dove $P$ è uno [[Stato|stato]] e $Y$ è un [[Simbolo|simbolo]] del [[Vocabolario|vocabolario]] $V$, tramite le seguenti regole:
- Se $Y$ è un terminale e $\tau(P, Y) = Q$ si inserisce la mossa `shift Q`
- Se $P$ contiene un [[Reducing item|reducing item]] per $A \rightarrow \beta$ e $Y \in \mathcal{LA}(P, A \rightarrow \beta)$, si inserisce la mossa `reduce A -> b` (le [[Reduce|reduce]] dipendono dalla *lookahead function* $\mathcal{LA}$)
- Se $P$ contiene l'*accepting item* e $Y = \$$ si inserisce `accept`
    - Nel caso degli [[Grammatica LR(0)|automi LR(0)]] l'accepting item è { $S' \rightarrow S \cdot$ }
    - Nel caso degli [[Grammatica LR(1)|automi LR(1)]] l'accepting item è { $S' \rightarrow S \cdot, \Delta$ }
- Se $Y$ è un terminale o $\$$ e nessuna delle condizioni precedenti è valida si inserisce `errore`
- Se $Y$ è un non-terminale e $\tau(P, Y) = Q$ si inserisce la mossa `goto Q`

## Conflitti

Esistono principalmente due tipi di conflitti possibili in una tabella di parsing:
- **Conflitti shift/reduce**: nel caso in cui almeno un entry $M[P, Y]$ della tabella di parsing contiene sia un'operazione di `shift Q` sia un operazione di `reduce A -> b`
- **Conflitti reduce/reduce**: nel caso in cui almeno un entry della tabella di parsing contiene due operazioni di `reduce` per produzioni distinte
