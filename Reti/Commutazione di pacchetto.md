---
 Created: 2022-12-09 18:48
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **commutazione di pacchetto** è una tecnica utilizzata in reti di [[Computer|computer]] per il **trasferimento di dati**

---

Il **flusso di dati** viene suddiviso in **pacchetti** che condividono le **risorse** di rete
Ciascun pacchetto utilizza **completamente** le risorse fisiche che vengono ripartite in modalità ***best effort*** ed a seconda della **necessità** (*on demand*)

La **richiesta** di risorse può **eccedere** il quantitativo disponibile

Per condividere le **risorse** vengono utilizzate diverse tecniche:
- **Multiplexing statico**: in cui la condivisione di risorse avviene su **richiesta** e la sequenza non segue uno schema prefissato
- ***Store-and-forward***: in cui il pacchetto viene **temporaneamente** memorizzato prima di essere inviato al nodo successivo
  L'**intero pacchetto** deve arrivare a destinazione prima di essere re-inviato e questo può causare [[Congestione della rete |congestione]]