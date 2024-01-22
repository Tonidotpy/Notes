---
 Created: 2023-04-18 10:15
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [scheduling]
---

Lo **scheduler** è un [[Programma|progamma]] che implementa un [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]] di [[Scheduling|scheduling]] e stabilisce un ordinamento temporale per l'esecuzione dei [[Processo|processi]]

---

Esistono tre tipi di scheduler:
1. **Short-term scheduler** (o *[[Central Process Unit|CPU]] scheduler*): seleziona quali sono i prossimi processi ad essere eseguiti
   Viene invocato molto di frequente ^7fc376
2. **Mid-term scheduler**: i [[Sistema operativo|SO]] con [[Memoria virtuale|memoria virtuale]] prevedono un livello intermedio di scheduling per la momentanea rimozione forzata (*swapping*) di un processo in esecuzione
3. **Long-term scheduler** (o *job scheduler*): seleziona quali processi devono essere trasferiti nella [[Coda|coda]] dei processi pronti
   Viene invocato meno frequentemente

---

Ogni processo gestito dallo scheduler viene inserito in una serie di code:
- [[Ready queue]] (o [[Coda|coda]] dei processi pronti): la coda dei processi pronti per l'esecuzione
  Un processo esce dalla ready queue quando smette di essere eseguito (*dispatched*)
- Coda di un dispositivo: la coda dei processi in attesa che il dispositivo si liberi

Durante un'operazione di dispatch da parte del [[Dispatcher|dispatcher]] avviene il [[Context switching|cambio di contesto]], in quel caso lo scheduler sceglie un nuovo processo da eseguire scambiandolo con quello vecchio