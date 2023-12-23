---
Created: 2023-12-23 19:29
Author: Antonio Gelain
aliases:
  - DFA
tags:
  - linguaggi-formali-e-compilatori
---

Un **automa a stati finiti deterministico** è un particolare tipo di [[Automa a Stati Finiti|macchina a stati finiti]] rappresentabile con una tupla
$$\mathcal{D} = (S, \mathcal{A}, \text{move}_{d}, S_{0}, F)$$
in cui:
- $S$ è un insieme di [[Stato|stati]]
- $\mathcal{A}$ è un [[Alfabeto|alfabeto]] con $\epsilon \notin \mathcal{A}$
- $s_{0} \in S$ è lo stato iniziale
- $F \subseteq S$ è l'insieme degli stati finiti o accettati
- $\text{move}_{d} : S \times \mathcal{A} \rightarrow S$ è la funzione di transizione da un certo stato e on un certo [[Simbolo|simbolo]]

---

Un DFA:
- Non presenta [[Epsilon transizione|epsilon transizioni]]
- Se $\text{move}_{d}$ è **totale**, allora per ogni stato, c'è **esattamente** una $a$-transizione $\forall a \in \mathcal{A}$
- Se $\text{move}_{d}$ è **parziale**, allora per ogni stato c'è al **massimo** una $a$-transizione $\forall a \in \mathcal{A}$

Un [[Linguaggio regolare|linguaggio]] $\mathcal{L(D)}$ riconosciuto da un DFA $\mathcal{D}$ è l'[[Analisi/Insiemi/Insieme|insieme]] delle parole $w$ tale che:
- Esiste un [[Cammino|cammino]], che chiamiamo $w$ la cui lunghezza è maggiore di 0, che vada dallo stato iniziale $S_{0}$ ad un qualche stato finale in $F$
- Vale che $S_{0} \in F \cap w = \epsilon$, perciò lo stato di partenza è uno stato finale ed è l'unico caso in cui un DFA riconosce una parola vuota