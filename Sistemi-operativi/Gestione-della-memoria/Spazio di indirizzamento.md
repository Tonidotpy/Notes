---
 Created: 2023-05-07 14:12
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

Lo **spazio di indirizzamento** è una lista di [[Indirizzo di memoria|indirizzi di memoria]] compresi tra un valore **minimo** ed un valore **massimo**

---

Lo spazio di indirizzamento può contenere:
- [[Indirizzo logico|Indirizzi logici]]
- [[Indirizzo fisico|Indirizzi fisici]]
Che possono essere diversi solamente nel [[Binding|binding]] a run-time

Nelle architetture moderne lo spazio di indirizzamento virtuale è di **molto maggiore** rispetto allo spazio fisico, per questo vengono utilizzati dei meccanismi per gestire questo problema, come ad esempio:
- La [[Tabella delle pagine multilivello|tabella delle pagine multilivello]]
- La [[Tabella delle pagine invertita|tabella delle pagine invertita]]