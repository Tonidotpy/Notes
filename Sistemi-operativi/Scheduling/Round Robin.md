---
 Created: 2023-04-23 14:30
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [scheduling, algoritmo]
---

**Round robin** è un [[Algoritmo|algoritmo]] di [[Scheduling|scheduling]] che assegna ad ogni [[Processo|processo]] una piccola parte (*quanto*) di tempo della [[Central Process Unit|CPU]]

---

Si tratta di un algoritmo [[Prelazione|preemptive]] in quanto, se al termine del quanto di tempo assegnato ad un processo questo non ha ancora terminato, la sua esecuzione viene **fermata temporaneamente** e il processo viene sostituito da un altro

La dimensione del quanto di tempo deve essere **scelta attentamente**, questo perché se il quanto è troppo grande avvengono pochi [[Context switching|context switches]], altrimenti se è troppo piccolo ne avvengono troppi, riducendo così le prestazioni