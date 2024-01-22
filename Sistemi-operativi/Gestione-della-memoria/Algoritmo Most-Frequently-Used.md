---
 Created: 2023-05-13 14:47
 Author: Antonio Gelain
 Aliases: [Algoritmo MFU]
 Tags: [gestione-della-memoria]
---

L'**algoritmo Most Frequently Used** (o *algoritmo MFU*) è un [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]] per la sostituzione delle [[Paginazione|pagine]] nel caso di [[Page fault|page fault]], che rimpiazza le pagine utilizzate più di recente

---

Per ogni pagina viene mantenuto un **conteggio** dei riferimenti e nel caso di page fault viene rimpiazzata la pagina con il conteggio più alto

Questo algoritmo si basa sul concetto che una pagina il cui conteggio è basso probabilmente è stata appena caricata e dovrà essere utilizzata ancora