---
Created: 2023-12-19 14:41
Author: Antonio Gelain
aliases:
  - Parsing
tags:
  - linguaggi-formali-e-compilatori
---

L'**analisi sintattica**(o *parsing*) è un meccanismo che permette di verificare se una **sequenza di [[Token|tokens]]** è valida rispetto ad una [[Grammatica generativa|grammatica]]

---

> [!INFO] È durante questa fase che compaiono i *syntax errors*

Se le regole della grammatica vengono rispettate, il flusso di token viene tradotto in un [[Albero di derivazione|parse tree]] (o meglio un [[Abstract Syntax Tree|AST]])

---

Esistono due principali categorie per il parsing, più un'ulteriore categoria la cui forma è più generale:
- [[Top-Down parsing]]
- [[Bottom-Up parsing]]
