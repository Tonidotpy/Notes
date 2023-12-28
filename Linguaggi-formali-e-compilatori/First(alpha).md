---
 Created: 2023-12-28 15:15
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

**First($\alpha$)** è l'[[Analisi/Insiemi/Insieme|insieme]] di [[Simbolo|terminali]] che sono posti all'inizio delle stringhe [[Derivazione|derivate]] da $\alpha$, definito per [[Principio di induzione|induzione]] nel seguente modo:
- **Caso base**
    - $first(\epsilon) = \epsilon$
    - $first(\alpha) = \alpha$
- **Passo induttivo**: $first(A) = \bigcup_{A \rightarrow \alpha} first(\alpha)$

---

Se $a \Rightarrow^{*} \epsilon$ allora $\epsilon \in first(\alpha)$, ciò vuol dire che $\alpha$ è un non-terminale **annullabile** (*nullable*) e quindi sarà pari ad $\epsilon$

Per calcolare l'insieme $first(Y_{1} ... Y_{n})$ (con $Y_{i} \in V$) bisogna iterare su tutti gli elementi $Y_{j} \in V$ della parola:
- Finché non abbiamo esaminato tutti gli $Y_{j} : 1 \le j \le n$, si aggiunge $first(Y_{j}) \backslash \{ \epsilon \}$ al'insieme
- Se $\epsilon \in first(Y_{j})$ allora è necessario continuare la ricerca dei first, perché è possibile che in almeno un caso $Y_{j} = \epsilon$ e quindi è possibile che nessuno dei $first(Y_{j}) \in first(Y_{1} ... Y_{n})$
- Altrimenti possiamo fermarci in quanto abbiamo trovato tutti i $first(Y_{1} ... Y_{n})$
Infine si verifica se tutti gli $Y_{j}$ sono annullabili e nel caso si aggiunge $\epsilon$ all'insieme in quanto anche $(Y_{1} ... Y_{n})$ sarebbe annullabile

In pseudo-codice:
```
function firstComputation(Word a) -> Set begin
    Set first(Y1 ... Yn) = 0
    j = 1

    % Per ogni Y calcolo il suo first %
    while j <= n do
        first(Y1 ... Yn).add(first(Yj) \ { e })

        % Se e appartiene al first di Yj passo al simbolo successivo %
        if e in first(Yj) then
            ++j
        else
            break
    done

    % Se ho utilizzato tutti i simboli aggiungo epsilon all'insieme %
    if j = n + 1 then first(Y1 ... Yn).add(e) fi
    return first(Y1 ... Yn)
end
```
