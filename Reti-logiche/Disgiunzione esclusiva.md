---
Created: 2023-09-30 18:55
Author: Antonio Gelain
aliases:
  - Operatore XOR
tags:
---

Una **disgunzione esclusiva logica** è un [[Operatore logico|connettivo logico]] attraverso il quale a partire da due proposizioni, si forma una nuova proposizione chiamata **disgunzione esclusiva** che assume il valore **vero** solamente quando le due proposizioni in input hanno valori **diversi** fra loro

---

Di seguito viene mostrata la tabella di verità dell'operatore XOR:

| $A$ | $B$ | $A \oplus B$ |
| --- | --- | ----------- |
| F   | F   | F           |
| F   | V   | V           |
| V   | F   | V           |
| V   | V   | F           |

L'operatore XOR può essere ricavato utilizzando tutti e tre gli operatori logici principali:
$$x \oplus y = x \land \lnot y \lor \lnot x \land y$$

Esiste una versione **negata** che si può ricavare utilizzando l'[[Negazione logica|operatore NOT]], che permette di invertire il [[Valore di verità|valore logico]] della congiunzione, chiamata **XNOR**
