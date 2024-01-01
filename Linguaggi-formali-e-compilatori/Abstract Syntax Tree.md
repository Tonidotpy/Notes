---
Created: 2024-01-01 14:06
Author: Antonio Gelain
aliases:
  - AST
  - Albero di sintassi astratta
tags:
  - linguaggi-formali-e-compilatori
---

Un **Abstract Syntax Tree** (o *AST* in breve) è un particolare tipo di [[Albero di derivazione|albero di derivazione]] più compatto

---

In un AST le foglie vengono salvate come dei *link* ai record nella [[Tabella dei simboli|tabella dei simboli]], i quali contengono identificatori o valori diretti (*e.g.* numeri, ...) della parola che stiamo [[Analisi sintattica|parsando]]
I nodi intermedi costituiscono la **struttura topologica** dell'albero e rappresentano tutte le operazioni compiute tra variabili e valori diretti

## Creazione di un AST

Un AST può essere creato semplificando l'albero di derivazione tramite delle operazioni di compattazione rimuovendo i nodi inutilizzati
Tuttavia, in genere, si preferisce creare l'AST durante l'[[Analisi sintattica|analisi sintattica]] e per fare ciò si ha bisogno delle [[Funzione di attribuzione|funzioni di attribuzione]]

Per ogni produzione utilizzata per ottenere la parola analizzata si applicano le funzioni di attribuzione appropriate costruendo passo-passo l'AST

Questo tipo di operazione, nel caso di una grammatica [[Grammatica LALR(1)|LALR(1) L-attribuita]] non funziona in quanto non è sempre possibile ricavare immediatamente i valori necessari per la costruzione dell'AST
