---
 Created: 2023-04-21 12:07
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [SRTF]
 Tags: [scheduling,algoritmo]
---

Come per l'[[Shortest-Job-First|SJF]] l'[[Algoritmo|algoritmo]] di **shortest remainig time first** (*SRTF*) sceglie il [[Processo|processo]] col tempo di esecuzione minore possibile ma nel caso arrivi un nuovo processo più rapido da eseguire di quello in esecuzione quest'ultimo viene rimosso dalla [[CPU]] e sostituito con quello appena arrivato

---

Questo tipo di algoritmo è [[Prelazione|preemptive]]