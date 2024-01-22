---
 Created: 2024-01-22 11:41
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **quantizzazione** è un processo di **mappatura** di valori in ingresso di un [[Segnale|segnale]] [[Campionamento|campionato]] in valori di un [[Analisi/Insiemi/Insieme|insieme]] più piccolo e numerabile, spesso con un numero finito di elementi
$$x(nT_{c}) = x_{q}(nT_{c}) + \epsilon_{q}(nT_{c})$$
dove:
- $x(nT_{c})$ è il segnale campionato
- $x_{q}(nT_{c})$ è il segnale quantizzato
- $\epsilon_{q}(nT_{c})$ è l'[[Errore di quantizzazione|errore di quantizzazione]]

---

>[!WARNING] La quantizzazione è sempre un'operazione [[Lossy|lossy]], ossia con perdita di [[Informazione|informazioni]]

Tipicamente si sceglie un set predefinito di $M$ possibili livelli come una potenza di 2, in modo da poterlo rappresentare con un numero i bit $B$ tale che $2^{B} = M$

L'assegnazione di ogni campione al livello corrispondente avviene secondo un **criterio di minima distanza**

Esistono due tipi di quantizzazioni:
1. [[Quantizzazione uniforme]]
2. [[Quantizzazione non uniforme]]
