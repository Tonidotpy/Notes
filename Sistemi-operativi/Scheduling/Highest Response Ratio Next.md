---
 Created: 2023-04-23 14:19
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [scheduling, algoritmo]
---

**Highest response ratio next** (*HRRN*) è un [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]] di [[Scheduling|scheduling]] di tipo [[Prelazione|non-preemptive]] il cui scopo è quello di mitigare la [[Starvation|starvation]] di un processo

---

La **priorità** ($R$) viene calcolata in base al **tempo di attesa** ($t_{attesa}$) e il **tempo di esecuzione** ($t_{burst}$) secondo la seguente formula:
$$R = \frac{t_{attesa} + t_{burst}}{t_{burst}} = 1 + \frac{t_{attesa}}{t_{burst}}$$