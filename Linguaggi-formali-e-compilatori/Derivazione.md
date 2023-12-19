---
Created: 2023-09-12 10:14
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---

Una **derivazione** ($\Rightarrow$) è una riscrittura delle stringhe contenenti [[Simbolo|caratteri non terminali]] in stringhe composte solamente da caratteri terminali

---

Si utilizza un **carattere speciale** ($\epsilon$) per rappresentare una **parola vuota** con le seguenti caratteristiche:
- $|\epsilon| = 0$
- $\epsilon = \epsilon \epsilon$
- $\epsilon = b^{0}$
- Il carattere $\epsilon$ non viene scritto nelle parole

---

Esistono due tipi di **derivazioni canoniche**:
1. **Rightmost** (si rimpiazzano sempre prima i non terminali più a destra)
2. **Leftmost** (si rimpiazzano sempre prima i non terminali più a sinistra)