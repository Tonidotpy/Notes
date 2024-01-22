---
Created: 2023-10-05 11:22
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---

Sia ($S, \mathcal{A}, \text{move}_{n}, S_{0}, F$) un [[Automa a Stati Finiti Non-deterministico|NFA]], sia $t$ uno stato in $S$ e $T$ un [[Sottoinsieme|sottoinsieme]] di $S$.
Definiamo **$\epsilon$-chiusura**($\{ t \}$) l'insieme di stati in $S$ che sono raggiungibili da $t$ tramite zero o più **$\epsilon$-transizioni**
$$\epsilon\text{-chiusura}(T) = \bigcup_{t \in T} \epsilon\text{-chiusura}(\{ t \})$$

---

Per calcolare un'$\epsilon$-chiusura servono:
- Uno [[Pila|stack]] dove memorizzare gli stati
- Un [[Array|array]] di [[Variabile booleana|booleani]] per memorizzare se uno stato è già stato visitato o meno
poi si procede col seguente [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]]:
1. Si aggiunge il nodo di partenza allo stack e lo si segna come visitato
2. Per ogni [[Epsilon transizione|epsilon transizione]] se lo stato successivo alla transizione non è stato visitato si ripete il procedimento ricorsivamente utilizzando il nuovo stato come nodo di partenza

Tradotto in pseudo-codice:
```
function e-chiusura(State {t}, Stack S) begin
    % Aggiungo il nodo allo stack e lo salvo come visitato %
    S.push(t)
    visited[t] = true
    
    % Attraverso ogni e-transizione del nodo corrente %
    foreach u in move(t, e) do
        if not visited[u] then
            e-chiusura(u, S)
        fi
    done
end
```

> [!INFO] La [[Complessità temporale|complessità]] del calcolo della $\epsilon$-chiusura è di $\mathcal{O}(n + m)$ dove $n$ è il numero di stati (nodi) dell'NFA mentre $m$ è il numero di transizioni (archi)

---

Si può definire la $\epsilon$-chiusura($M$), dato $N = (S, \mathcal{A}, \text{move}_{n}, S_{0}, F)$ un NFA e $M \subseteq S$, come il **più piccolo** insieme di $X \subseteq S$ tale che $X$ è una soluzione alla seguente equazione:
$$X = M \cup \{ N'\ |\ N \in X \cap N' \in \text{move}_{n}(N, \epsilon) \}$$

Si può notare come la definizione di $X$ dipenda da $X$ stessa, per questo è importante notare che si prende il più piccolo insieme in modo da evitare [[Ciclo|cicli]] infiniti
A questo proposito entra in gioco il [[Linguaggi-formali-e-compilatori/Teorema del punto fisso|teorema del punto fisso]]