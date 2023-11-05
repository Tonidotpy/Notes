---
Created: 2023-11-05 12:24
Author: Antonio Gelain
aliases: 
tags:
  - logica-computazionale
---

Una **regola di formazione** è una regola che descrive quali stringhe di [[Simbolo|simboli]] formate da un [[Alfabeto|alfabeto]] sono **sintatticamente valide**

---

Nel caso delle [[Grammatica libera|grammatiche libere]] possiamo definire la regola di formazione, utilizzando la notazione [[Backus-Naur Form|BNF]], nel seguente modo:
$$\langle \text{expression} \rangle \Coloneqq \text{-- expression --}$$
dove:
- $\langle \text{expression} \rangle$ è un espressione **non terminale**
- $\text{-- expression --}$ consiste in una o più simboli **terminali** oppure **non terminali**
