---
 Created: 2023-12-28 19:18
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **grammatica con fattorizzabilità sinistra** è un tipo di [[Grammatica libera|grammatica]] che può essere **fattorizzata a sinistra**, ossia quando:
- Ci sono almeno due [[Produzione|produzioni]] che hanno lo stesso non-terminale come *driver*
- Possiedono un prefisso comune come *body*

---

> [!INFO] Se la grammatica $\mathcal{G}$ può essere fattorizzata a sinistra, allora **sicuramente** $\mathcal{G}$ **NON** è [[Grammatica LL(1)|LL(1)]]

Per applicare una fattorizzazione a sinistra ad una grammatica bisogna, per ogni non-terminale della grammatica:
- Trovare il più lungo prefisso $\alpha$ in comune a due o più produzioni aventi lo stesso *driver*
- Se tale prefisso $\alpha$ esiste allora:
    - Viene scelto un non-terminale $A' : A' \notin \mathcal{A}\ \backslash\ T$
    - Si sostituiscono tutte le produzioni di $A$ nella forma $A \rightarrow \alpha \beta_{1}\ |\ ...\ |\ \alpha \beta_{n}\ |\ \gamma_{1}\ |\ ...\ |\ \gamma_{n}$
      con le seguenti produzioni: $A \rightarrow \alpha A'\ |\ \gamma_{1}\ |\ ...\ |\ \gamma_{n}$ e $A' \rightarrow \beta_{1}\ |\ ...\ |\ \beta_{n}$
- Si ripete tutto il procedimento finché non è più possibile trovare produzioni con un prefisso comune

In pseudo-codice:
```
repeat
    foreach A do
        % Cerca il più grande prefisso a in comune a due o più produzioni per A %
        if a != e then
            %%%
            Scegli un nuovo non-terminale A' e rimpiazza
            A -> a b1 | ... | a bn | y1 | ... | yn con
            A -> a A' | y1 | ... | yn
            A' -> b1 | ... | bn 
            %%%
        fi
    done
until no pair of productions for any A has common prefix
```

## Eliminazione della fattorizzabilità sinistra

Data una grammatica $\mathcal{G}$ che ha due produzioni con lo stesso driver e prefisso comune, quello che si fa è rimpiazzare la produzione iniziale
$$A \rightarrow \alpha \beta_{1}\ |\ \alpha \beta_{2}$$
andando a sostituirla con due produzioni di questo tipo:
$$
\begin{matrix}
A \rightarrow \alpha A' \\
A' \rightarrow \beta_{1}\ |\ \beta_{2}
\end{matrix}
$$
dove $A'$ è un non-terminale nuovo diverso da quelli già presenti nella grammatica di partenza
