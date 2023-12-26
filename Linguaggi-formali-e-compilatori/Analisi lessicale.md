---
 Created: 2023-12-19 14:36
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

L'**analisi lessicale** è un meccanismo che permette di tradurre un **flusso di caratteri** in un **flusso di [[Token|tokens]]**

---

Durante questa fase non vengono perse informazioni ma vi si assegna dei ruoli ai vari token

Durante la fase di analisi lessicale vengono analizzati i [[Lessema|lessemi]] che possono facilmente essere descritti utilizzando [[Espressione regolare|espressioni regolari]] e di conseguenza permettono di costruire una [[Automa a Stati Finiti|macchina a stati finiti]] che li riconosce

In alcuni casi è possibile che venga analizzato un carattere che non fa parte del token corrente ma che comunque lo valida, in quel caso bisogna ritornare indietro al carattere precedente, questa operazione viene chiamata **retract**
