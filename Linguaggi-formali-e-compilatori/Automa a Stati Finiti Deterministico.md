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

---

## Dimensione di un DFA

Per ogni $n \in \mathbb{N}^{+}$ esiste un [[Automa a Stati Finiti Non-deterministico|NFA]] con ($n + 1$) stati il cui DFA **minimo** equivalente ha almeno $2^{n}$ stati

### Dimostrazione

Prendiamo ad esempio il linguaggio regolare:
$$\mathcal{L} = \mathcal{L}((a | b)^{*} a (a|b)^{n-1})$$

Esiste un NFA con **esattamente** $n + 1$ stati che accetta il linguaggio $\mathcal{L}$
Supponiamo per assurdo che esista un DFA minimo $\mathcal{D}$ che accetti il linguaggio $\mathcal{L}$ ed abbia $k < 2^{n}$ stati
Sappiamo esserci esattamente $2^{n}$ parole distinte su $\{ a, b \}$ la cui lunghezza è $n$

Esistono quindi $2$ percorsi in $\mathcal{D}$ tali che:
- La loro lunghezza è $n$
- Compongono rispettivamente le parole $w_{1}$ e $w_{2}$, con $w_{1} \ne w_{2}$
- Condividono almeno un arco

Se non esistessero, allora i nodi sarebbero come minimo $2^{n}$; di conseguenza per qualche $x_{1}$, $x_{2}$ e $x$ vale una delle due opzioni seguenti:
- $w_{1} = x_{1} a x$ e $w_{2} = x_{2} b x$
- $w_{1} = x_{1} b x$ e $w_{2} = x_{2} a x$
altrimenti le due parole sarebbero uguali.

Supponiamo in questo caso che sia valida la condizione:
$$
\begin{matrix}
w_{1} = x_{1} a x & w_{2} = x_{2} b x
\end{matrix}
$$
allora possiamo definire $w_{1}'$ in questo modo:
$$w_{1}' = x_{1} a b^{n-1} \in \mathcal{L(D)}$$

Di conseguenza, lo stato nuovamente aggiunto da $w_{1}'$ in $\mathcal{D}$ è uno **stato finale**.
La precedente affermazione è una **contraddizione**: lo stato non può essere finale, perché può essere raggiunto anche tramite $x_{2} b b^{n-1}$, ma
$$x_{2} b b^{n-1} \notin \mathcal{L(D)}$$
