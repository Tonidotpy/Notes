---
 Created: 2023-12-25 14:10
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

**Subset construction**[^online-tool] è un [[Algoritmo|algoritmo]] utilizzato per ricavare un [[Automa a Stati Finiti Deterministico|DFA]] $\mathcal{D}'$ dato un certo [[Automa a Stati Finiti Non-deterministico|NFA]] $\mathcal{D}$ tale che $\mathcal{L(D) = L(D')}$

---

> [!INFO] La [[Complessità temporale|complessità]] di questo algoritmo è di $\mathcal{O}(2^{n} \cdot |A| \cdot (n + m))$ con $n$ il numero di stati ed $m$ il numero di transizioni dell'NFA

L'algoritmo è il seguente:
1. Si calcola la [[Epsilon chiusura di un automa|epsilon chiusura]] dello stato iniziale e lo si pone come stato iniziale del DFA
2. Per ogni stato del DFA non controllato (*unmarked*), si segna come visitato (*marked*)
3. Per ogni [[Simbolo|simbolo]] dell'[[Alfabeto|alfabeto]] si calcola la $\epsilon$-chiusura di tutte le transizioni contenenti quel simbolo degli stati dell'NFA che hanno generato il nodo corrente del DFA, che viene interpretato come uno stato del DFA
4. Se l'$\epsilon$-chiusura calcolata è vuota oppure è uno stato del DFA già visitato allora si passa al prossimo simbolo
5. Altrimenti si aggiorna la transizione dallo stato corrente del DFA col simbolo corrente col nuovo stato del DFA calcolato e lo si segna come non marcato
6. Infine una volta terminato tutto il procedimento si segnano gli stati finali del DFA tutti i nodi che contengono stati finali dell'NFA di partenza

In pseudo-codice:
```
% Calcolo la epsilon chiusura dello stato iniziale %
T0 = e-chiusura({S0})
R = T0

% Per ogni stato 'unmarked' del DFA %
while qualche T in R è unmarked do
    mark(T)
    
    % Per ogni simbolo dell'alfabeto %
    for a in A do
        % Calcolo il prossimo stato tramite la epsilon chiusura %
        T' = e-chiusura(U_{t in states} move_d(t, a))
        if T' != 0 then
            % Aggiorno le transizioni del DFA %
            move_d(T, a) = T'
            if T' in R then
                add T' to R
                unmark(T')
            fi
        fi
    done
done
foreach T in R do
    if (T ∩ F) != 0 then
        set T in E
    fi
done
```

> [!WARNING] L'algoritmo di subset construction ricava **una possibile soluzione** ma non è detto che questa sia la migliore


[^online-tool]: Strumento online per la generazione di un DFA da un NFA: https://cyberzhg.github.io/toolbox/nfa2dfa
