---
 Created: 2023-01-14 17:51
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

L'**analisi ammortizzata** è una tecnica di [[Complessità di un algoritmo|analisi di complessità]] che valuta il tempo richiesto per eseguire, nel **caso pessimo**, una sequenza di operazioni su una [[Struttura di dati|struttura dati]]

---

A differenza di un analisi di complessità normale non si valuta una singola operazione ma una serie di **operazioni multiple** che possono anche essere molto costose ma la cui frequenza è bassa e perciò il costo totale può essere **ammortizzato**

Esistono diversi metodi per l'analisi ammortizzata:
- [[Metodo dell'aggregazione]]
- [[Metodo degli accantonamenti]]
- [[Metodo del potenziale]]