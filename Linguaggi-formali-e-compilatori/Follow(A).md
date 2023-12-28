---
 Created: 2023-12-28 16:02
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

**Follow(A)** è l'[[Analisi/Insiemi/Insieme|insieme]] di [[Simbolo|terminali]] che possono seguire $A$ in qualche [[Derivazione|derivazione]]

---

A differenza dei [[First(alpha)|first]], i follow sono computati **solamente** per i non-terminali

L'[[Algoritmo|algoritmo]] per calcolare il follow inizializza il $follow(S) = \{ \$ \}$ dal momento che dallo *start-symbol* si possono generare tutte le possibili parole appartenenti al linguaggio allora possiamo aspettarci di trovare il terminatore di stringa $ dopo una qualsiasi parola

A questo punto, dato che siamo interessati solamente a quali terminali seguono un particolare non terminale, ci interessano solamente le [[Produzione|produzioni]] della [[Grammatica generativa|grammatica]] per cui il generico non terminale $A$ compare nel *body*

Per ogni $B \rightarrow \alpha A \beta$, si eseguono le seguenti operazioni:
- Se $\beta \ne \epsilon$ allora aggiungamo $first(\beta)\ \backslash\ \{ \epsilon \}$ a $follow(A)$
- Se $\beta = \epsilon$ oppure $\epsilon \in first(\beta)$ allora aggiungiamo $follow(B)$ a $follow(A)$, questo perché ciò che segue $B$ potrà seguire anche $A$

In pseudo-codice:
```
function followComputation(Word A) -> Set begin
    % Inizializza il follow dello start symbol con un insieme contenente un carattere terminatore e gli altri con l'insieme vuoto %
    Set follow(S) = { $ }
    foreach A != S do
        follow(A) = 0

    repeat
        foreach B -> aAb do
            % Aggiungo il first di beta (escluso epsilon) al follow di A se epsilon non appartiene a b %
            if b != e then
                follow(A).add(first(b) \ { e })
            fi
            
            % Aggiungo il follow di B al follow di A se epsilon è uguale a b oppure appartiene al first di b %
            if b = e or e in first(b) then
                follow(A).add(follow(B))
            fi
        done
    until saturation
end
```
