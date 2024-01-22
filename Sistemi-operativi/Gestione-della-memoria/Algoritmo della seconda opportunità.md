---
 Created: 2023-05-13 14:53
 Author: Antonio Gelain
 Aliases: [Algortimo della seconda scelta, Algoritmo dell'orologio, Algoritmo second chance]
 Tags: [gestione-della-memoria]
---

L'**algoritmo della seconda opportunità** (o *algoritmo dell'orologio*) è un [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]] per la sostituzione delle [[Paginazione|pagine]] nel caso di [[Page fault|page fault]], che utilizza uno o più [[Bit|bit]] di riferimento per decidere quali pagine sostituire

---

Questo tipo di algoritmo si basa su una [[Coda|coda]] circolare, nel caso in cui avvenga un page fault se trova una pagina il cui bit è a `1` lo pone a `0`, la **mantiene** in memoria e passa alla successiva, altrimenti se è gia a `0` la scambia con la pagina nuova