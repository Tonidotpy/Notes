---
 Created: 2023-04-23 15:03
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [scheduling, algoritmo]
---

La **coda multilivello** è una classe di [[Algoritmo|algoritmi]] in cui la [[Ready queue|ready queue]] viene partizionata in più [[Coda|code]] con un proprio algoritmo di [[Scheduling|scheduling]]

---

Oltre alla versione normale in cui ogni [[Processo|processo]] viene assegnato definitivamente ad una coda esiste una versione di coda multilivello con **feedback** (o *adattiva*)
In una **coda multilivello con feedback** un processo può spostarsi da una coda all'altra a seconda delle sue caratteristiche, ciò viene usato anche per implementare l'[[Aging|aging]]