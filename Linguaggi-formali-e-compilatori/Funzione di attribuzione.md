---
Created: 2024-01-01 14:28
Author: Antonio Gelain
aliases:
  - Regola semantica
  - Azione semantica
tags:
  - linguaggi-formali-e-compilatori
---

Una **funzione di attribuzione** (o *regola semantica*) è una [[Funzione|funzione]] che indica quando e come instanziare un nodo di un [[Abstract Syntax Tree|AST]], ogniqualvolta avviene una riduzione durante il [[Analisi sintattica|parsing]]

---

Le regole più significative sono:
- La regola che crea una nuova foglia $newLeaf(id, id.value)$
- La regola che crea un nuovo nodo interno $newNode(sym, left, right)$
