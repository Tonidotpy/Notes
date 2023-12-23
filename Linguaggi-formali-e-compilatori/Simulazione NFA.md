---
 Created: 2023-12-23 15:41
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **simulazione NFA** è un processo per cui viene verificata se una parola $w$ fa parte di un [[Linguaggio regolare|linguaggio]] di un dato [[Automa a Stati Finiti Non-deterministico|automa]] $\mathcal{N}$

---

L'[[Algoritmo|algoritmo]] per la simulazione NFA è il seguente:
1. Si calcola la [[Epsilon chiusura di un automa|epsilon chiusura]] dello stato iniziale
2. Si prende il primo carattere della stringa $w$
3. Finché non ho consumato tutti i caratteri della stringa ricalcolo la epsilon chiusura di tutti gli stati raggiungibili tramite una transizione contenente il carattere corrente e lo consumo
4. Infine se l'epsilon chiusura contiene uno [[Stato|stato]] finale allora $w \in \mathcal{L(N)}$ altrimenti $w \notin \mathcal{L(N)}$

In pseudo-codice:
```
% Calcolo l'epsilon chiusura dello stato iniziale e consumo il primo carattere della stringa %
states = e-chiusura({s0})
symbol = nextChar()

% Finche non ho consumato tutti i caratteri della stringa
while symbol != $ do
    % Calcolo la epsilon chiusura di tutti gli stati che posso raggiungere dallo stato corrente col carattere attuale %
    states = e-chiusura(U_{t in states} move_n(t, symbol))
    symbol = nextChar()
done

% Controllo se ho raggiunto uno stato finale %
if states ∩ F != 0 then
    return true
else
    return false
fi
```

> [!INFO] La [[Complessità temporale|complessità]] di una simulazione NFA è pari a $\mathcal{O}(|w||r|)$ con $|w|$ la lunghezza della parola da analizzare e $|r|$ la lunghezza dell'espressione regolare
