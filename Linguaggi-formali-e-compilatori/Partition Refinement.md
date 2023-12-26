---
 Created: 2023-12-25 14:50
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

**Partition refinement**[^online-tool] è una procedura utilizzata per eliminare gli [[Stato|stati]] in eccesso di un [[Automa a Stati Finiti Deterministico|DFA]] senza modificarne il [[Linguaggio regolare|linguaggio]] descritto

---

Grazie a questa procedura arriveremo a partizionare gli stati in 2 blocchi

1. Iniziamo con due blocchi generici $B_{1} = F$ e $B_{2} = S\ \backslash\ F$, questo fa sì che i due blocchi non abbiano stati equivalenti
2. Proseguiamo controllano se un blocco ha stati non equivalenti; se sì, li dividiamo in blocchi distinti separando tra di loro gli stati non equivalenti, e ripetiamo la procedura per i nuovi blocchi finché non ci sono più blocchi con stati non equivalenti

In pseudo codice:
```
% Set iniziali %
SET B1 = F
SET B2 = S \ F
SET P = { B1, B2 }

% Divido i blocchi finché non ce ne sono più con stati non equivalenti %
while qualche Bi in P può essere spezzato rispetto a qualche (a, Bj) do
    P.remove(Bi)
    P.insert({s in Bi : move_{d}(s, a) in Bj})
    P.insert({s in Bi : move_{d}(s, a) not in Bj})
done
```


[^online-tool]: Strumento online per la generazione di un DFA minimo: https://cyberzhg.github.io/toolbox/min_dfa
