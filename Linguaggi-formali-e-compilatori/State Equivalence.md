---
 Created: 2023-12-25 14:33
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Sia $\mathcal{D} = (S, \mathcal{A}, \text{move}_{d}, s_{0}, F)$ un [[Automa a Stati Finiti Deterministico|DFA]] con [[Funzione di transizione|funzione di transizione totale]].
Allora due [[Stato|stati]] $s, t \in S$ si dicono **equivalenti** *se e solo se* la seguente condizione è verificata:
$$\text{move}_{d}^{*}(s, x) \in F \iff \text{move}_{d}^{*}(t, x) \in F, \forall x \in \mathcal{A}^{*}$$
dove la funzione multi-passo $\text{move}_{d}^{*}$ è definita per [[Principio di induzione|induzione]] sulla lunghezza della stringa:
- **Passo base**: $\text{move}_{d}^{*}(s, \epsilon) = s$
- **Passo induttivo**: $\text{move}_{d}^{*}(s, wa) = \text{move}_{d}(\text{move}_{d}^{*}(s, w), a)$

---

