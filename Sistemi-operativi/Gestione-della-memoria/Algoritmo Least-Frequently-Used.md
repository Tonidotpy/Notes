---
 Created: 2023-05-13 14:42
 Author: Antonio Gelain
 Aliases: [Algoritmo LFU]
 Tags: [gestione-della-memoria]
---

L'**algoritmo Least Frequently Used** (o *algoritmo LFU*) è un [[Algoritmo|algoritmo]] per la sostituzione delle [[Paginazione|pagine]] nel caso di [[Page fault|page fault]], che rimpiazza le pagine utilizzate meno di recente

---

Per ogni pagina viene mantenuto un **conteggio** dei riferimenti e nel caso di page fault viene rimpiazzata la pagina con il conteggio più basso