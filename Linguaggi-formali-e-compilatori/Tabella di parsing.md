---
 Created: 2023-12-27 20:56
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **tabella di parsing** è un particolare tipo di tabella che viene utilizzata dai [[Top-Down parsing predittivo|parser top-down predittivi]] per analizzare una [[Grammatica LL(1)|grammatica LL(1)]]

---

La tabella è composta nel seguente modo:
- Si ha una **riga** per ogni **non-terminale** della grammatica
- Si ha una **colonna** per ogni **terminale** della grammatica, a cui si aggiunge il simbolo `$` utilizzato come terminatore
- Le celle vuote all'interno della tabella identificano casi di errore

All'interno di una cella identificata da un [[Simbolo|simbolo]] non-terminale $A$ ed un terminale $b$ è presente la produzione $M[A, b] = A \rightarrow a$ se:
- Il *body* della produzione con *driver* $A$ è tale per cui esiste una derivazione del tipo $\alpha \Rightarrow^{*} b \beta$, ossia partendo da $\alpha$ si riesce, con zero o più passi, a ottenere una stringa che inizia per $b$
- Oppure $\alpha \Rightarrow^{*} \epsilon$ ed è possibile avere $S \Rightarrow^{*} wAy$ con $\gamma \Rightarrow^{*} b \beta$

---

Per costruire una tabella di parsing si scorrono tutte le produzioni $A \rightarrow \alpha$ presenti nella grammatica e, per ognuna di queste (utilizzando il [[First(alpha)|first]] e il [[Follow(A)|follow]]):
- Si aggiunge $A \rightarrow \alpha$ in $M[A, b]$ per ogni $b \in (first(\alpha)\ \backslash\ \{ \epsilon \})$
- Se $\epsilon \in first(\alpha)$, si aggiunge $A \rightarrow \alpha$ a $M[A, x]$ per tutti gli $x \in follow(A)$

In pseudo-codice:
```
function parsingTableComputation(Grammar G) -> Table begin
    foreach A -> a in P do
        % Per ogni simbolo in first(a) si aggiunge la produzione alla tabella %
        foreach b in (first(a) \ { e }) do
            add A -> a to M[A, b]
        done

        % Se epsilon appartiene a first(a) allora per ogni simbolo in follow(A) si aggiunge la produzione alla tabella %
        if e in first(a) then
            foreach x in follow(A) do
                add A -> a to M[A, x]
            done
        fi
    done

    % Assegna error() a tutte le celle vuote rimanenti %
end
```
