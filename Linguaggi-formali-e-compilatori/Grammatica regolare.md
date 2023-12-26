---
Created: 2023-09-29 09:07
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---

Una **grammatica regolare** è un particolare tipo di [[Grammatica libera|grammatica libera]] tale che le sue produzioni sono in una delle seguenti forme:
- Il *body* è un solo [[Simbolo|terminale]] ($A \mapsto a$)
- Il *body* è composto da un terminale e un non-terminale, nella seguente forma ($A \mapsto aB$)
- Il *body* è la parola vuota ($A \mapsto \epsilon$)

---

In genere i [[Linguaggi-formali-e-compilatori/Linguaggio|linguaggi]] generati da queste grammatiche sono riconosciuti dagli [[Automa a Stati Finiti|automi a stati finiti]], sia deterministici che non deterministici
