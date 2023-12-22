---
 Created: 2023-12-22 19:10
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Un'**espressione regolare** è una sequenza di [[Simbolo|simboli]] che identifica un [[Analisi/Insiemi/Insieme|insieme]] di stringhe e possono definire **tutti e soli** i [[Linguaggio regolare|linguaggi regolari]]

---

> [!IMPORTANT] Un'espressione regolare si dice che ==**denota**== un linguaggio, non che lo genera

Un'espressione regolare può essere definita per [[Principio di induzione|induzione]] nel seguente modo:
- **Caso base**: Sono un'espressione regolare tutti i simboli dell'alfabeto scelto più $\epsilon$
- **Passo induttivo**: Se $r_{1}$ e $r_{2}$ sono espressioni regolari
    - $r_{1}\ |\ r_{2}$ è un'espressione regolare, detta **alternanza**
    - $r_{1} \cdot r_{2}$ è un'espressione regolare, scritta anche come $r_{1} r_{2}$ ed è detta **concatenazione**
    - $r_{1}^{*}$ è un espressione regolare che significa **ripetizione** di $r$ per un certo numero di $k$ volte, detta ***Kleene star***
    - $(r_{1})$ è un'espressione regolare, usata per definire l'ordine di svolgimento delle operazione ed è detta **parentesi**

>[!INFO] In assenza di parentesi l'ordine di precedenza delle operazioni precedentemente descritte è la seguente:
> $$\text{Kleene Star < Concatenazione < Alternanza}$$