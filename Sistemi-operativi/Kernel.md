---
 Created: 2023-04-15 10:51
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **kernel** è il **nucleo** di un [[Sistema operativo|sistema operativo]], ovvero il software che fornisce un accesso sicuro e controllato dell'[[Hardware|hardware]] ai [[Processo|processi]] in esecuzione

---

Nei sistemi basati su kernel esistono **due** soli **livelli**:
1. Servizi **kernel**
2. Servizi **non-kernel**
Questo permette di avere alcuni vantaggi del [[Sistemi a livelli|sistema a livelli]] riducendone gli svantaggi dovuti alla difficoltà di definizione
Si tratta comunque di un sistema complesso che tende a diventare [[Kernel monolitici|monolitico]]

Un kernel può essere implementato in modo che venga eseguito:
- **Separatamente**: ossia "al di fuori" di ogni processo in modo che abbia uno spazio riservato in memoria e abbia la priorità su tutti gli altri processi
- All'interno di un **processo utente**: i servizi del SO sono **procedure chiamabili** da programmi utente accessibili in modalità protetta
- Come **processo**: i servizi del SO sono **processi individuali** eseguiti in modalità protetta