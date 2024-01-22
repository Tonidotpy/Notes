---
 Created: 2023-04-17 17:28
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [scheduling]
---

Lo **scheduling** è una tecnica di **gestione** dei [[Processo|processi]] il cui fine è quello di massimizzare l'utilizzo della [[Central Process Unit|CPU]] commutandola frequentemente tra processi

---

Lo scheduling in un [[Sistema operativo|SO]] viene generalmente implementato tramite uno [[Scheduler|scheduler]]

Lo scheduling può essere di tre tipi:
1. **Breve termine**
2. **Medio termine**
3. **Lungo termine**

Lo scheduling può essere con o senza [[Prelazione|prelazione]]

Nel caso in cui si abbiano più gruppi di processi le risorse vengono gestite **per gruppo** da un **fair share scheduler** che gestisce la quantità di risorse utilizzate per gruppi di processi che a loro volta verranno gestiti da dei normali scheduler

Alcune metriche valide per lo scheduling sono:
- L'**utilizzo della CPU**: si cerca di tenere la CPU il più occupata possibile
- Il **throughput**: numero di processi completati per unità di tempo
- **Tempo di attesa**: la quantità totale di tempo spesa da un processo in attesa
- **Tempo di completamento** (o *turnaround*): tempo necessario ad eseguire un particolare processo dall'inizio alla fine
- **Tempo di risposta**: tempo tracorso da quando una richiesta è stata sottoposta al sistema fina alla prima risposta del sistema stesso

---

Alcuni possibili [[Algoritmi-e-strutture-dati/Algoritmo|algoritmi]] di scheduling sono i seguenti:
- [[First Come First Served|FCFS]]
- [[Shortest Job First|SJF]]
- [[Shortest Remaining Time First|SRTF]]
- [[Highest Response Ratio Next|HRRN]]
- [[Round Robin|RR]]

Esistono diversi modi di **valutare** le performance di tali algoritmi:
- [[Modello deterministico]]
- [[Modello a reti di code]]
- [[Simulazione]]
- [[Implementazione]]