---
 Created: 2023-04-18 10:15
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Lo **scheduler** è un [[Programma|progamma]] che implementa un [[Algoritmo|algoritmo]] di [[Scheduling|scheduling]] e stabilisce un ordinamento temporale per l'esecuzione dei [[Processo|processi]]

---

Esistono due tipi di scheduler:
1. **Long-term scheduler** (o *job scheduler*): seleziona quali processi devono essere trasferiti nella [[Coda|coda]] dei processi pronti
   Viene invocato meno frequentemente
2. **Short-term scheduler** (o *[[CPU]] scheduler*): seleziona quali sono i prossimi processi ad essere eseguiti
   Viene invocato molto di frequente

Ogni processo gestito dallo scheduler viene inserito in una serie di code:
- **Ready queue** (o coda dei processi pronti): la coda dei processi pronti per l'esecuzione
  Un processo esce dalla ready queue quando smette di essere eseguito (*dispatched*)
- Coda di un dispositivo: la coda dei processi in attesa che il dispositivo si liberi

Durante un'operazione di dispatch avviene il [[Context switching|cambio di contesto]], in quel caso lo scheduler sceglie un nuovo processo da eseguire scambiandolo con quello vecchio