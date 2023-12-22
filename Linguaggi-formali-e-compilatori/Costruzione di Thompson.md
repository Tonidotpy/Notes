---
 Created: 2023-10-01 15:03
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **costruzione di Thompson** è una [[Algoritmo|procedura algoritmica]] che permette di costruire l'[[Automata|automata]] $\mathcal{N}$, che genera lo stesso [[Linguaggi-formali-e-compilatori/Linguaggio|linguaggio]] denotato da una certa [[Grammatica regolare#Espressioni regolari|espressione regolare]] $r$, ovvero $\mathcal{L(\mathcal{N})} = \mathcal{L}(r)$

---

Questa costruzione viene espressa in maniera [[Principio di induzione|induttiva]], come segue:

- **Caso base**: L'espressione regolare $r$ è:
    - $\epsilon$
    - Un simbolo dell'alfabeto $a \in \mathcal{A}$

Assumiamo di avere sempre un [[Automa a Stati Finiti Non-deterministico|NFA]] che riconosce $\mathcal{L}(\epsilon)$ e uno che riconosce $\mathcal{L}(a)\ \forall a \in \mathcal{A}$
- **Passo induttivo**: L'espressione regolare $r$ è una tra le seguenti opzioni:
    - $r_{1}\ |\ r_{2}$
    - $r_{1}r_{2}$
    - $r_{1}^{*}$
    - $(r_{1})$

![costruzione-di-Thompson](https://slidetodoc.com/presentation_image/93492c98dccdb1cb96b8109c88f01d46/image-30.jpg)