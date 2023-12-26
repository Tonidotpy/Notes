---
Created: 2023-10-01 15:03
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---

La **costruzione di Thompson**[^online-tool] è una [[Algoritmo|procedura algoritmica]] che permette di costruire l'[[Automata|automata]] $\mathcal{N}$, che genera lo stesso [[Linguaggi-formali-e-compilatori/Linguaggio|linguaggio]] denotato da una certa [[Espressione regolare|espressione regolare]] $r$, ovvero $\mathcal{L(\mathcal{N})} = \mathcal{L}(r)$

---

Questa costruzione viene espressa in maniera [[Principio di induzione|induttiva]], come segue:

- **Caso base**: L'espressione regolare $r$ è:
    - $\epsilon$
    - Oppure un simbolo dell'alfabeto $a \in \mathcal{A}$

Assumiamo di avere sempre un [[Automa a Stati Finiti Non-deterministico|NFA]] che riconosce $\mathcal{L}(\epsilon)$ e uno che riconosce $\mathcal{L}(a)\ \forall a \in \mathcal{A}$
- **Passo induttivo**: L'espressione regolare $r$ è una tra le seguenti opzioni:
    - $r_{1}\ |\ r_{2}$
    - $r_{1}r_{2}$
    - $r_{1}^{*}$
    - $(r_{1})$

> [!INFO] In ogni stato intermedio dell'NFA c'è **esattamente** uno stato finale senza archi uscenti, mentre lo stato iniziale non ha archi entranti

![costruzione-di-Thompson](https://slidetodoc.com/presentation_image/93492c98dccdb1cb96b8109c88f01d46/image-30.jpg)

> [!INFO] La [[Complessità temporale|complessità]] della costruzione di Thompson è $\mathcal{O}(|r|)$ con $|r|$ la lunghezza dell'espressione regolare


[^online-tool]: Strumento online per la generazione di un NFA da un'espressione regolare: https://cyberzhg.github.io/toolbox/regex2nfa
