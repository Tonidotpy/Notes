---
 Created: 2023-12-23 19:53
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **simulazione DFA** è un processo per cui viene verificata se una parola $w$ fa parte di un [[Linguaggio regolare|linguaggio]] di un dato [[Automa a Stati Finiti Deterministico|automa]] $\mathcal{N}$

---

Per un DFA con transizione **totale** abbiamo la certezza che per ogni [[Simbolo|simbolo]] che leggiamo ci sia un qualche arco che lo colleghi ad uno [[Stato|stato]] nel [[Grafo|grafo]], pertanto è sufficiente partire dallo stato iniziale $S_{0}$ e seguire il cammino dato dagli elementi di $w$, se terminano in uno stato finale in $F$ allora $w$ appartiene al linguaggio

> [!INFO] La [[Complessità temporale|complessità]] per una simulazione DFA è di $\mathcal{O}(|w|)$ con $|w|$ la lunghezza della parola

Per un DFA con transizione **parziale** bisogna considerare la possibilità di arrivare a uno stato in cui non si può più proseguire, perciò se stiamo leggendo un qualche simbolo per cui non c'è una transizione *etichettata* da quel simbolo possiamo direttamente ritornare una risposta negativa, altrimenti si procede come per la transizione totale
