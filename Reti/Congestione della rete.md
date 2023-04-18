---
 Created: 2022-12-10 17:14
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **congestione di rete** è una situazione che si verifica quando c'è troppo **traffico** su una rete, causando **ritardi** nella trasmissione dei dati e una riduzione delle **prestazioni** della rete

---

Ci sono **quattro** possibili cause per il **ritardo** dei pacchetti:
1. **Ritardo di elaborazione del nodo**: per via del **controllo errori** sui bit e per la determinazione della porta o del canale di uscita
2. **Ritardo di accodamento**: per l'**attesa della trasmissione** e per il livello di congestione del [[Router|router]] 
3. **Ritardo di trasmissione (L/R)**: dove `R` è la **frequenza** di trasmissione del collegamento (in `bit/s`) mentre `L` è la **lunghezza del pacchetto** (in `bit`)
4. **Ritardo di propagazione (d/s)**: dove `d` è la **lunghezza del collegamento** fisico mentre `s` è la **velocità di propagazione** del collegamento

---

Se la coda di attesa di un nodo è piena e arriva un altro pacchetto questo viene **scartato** per poi essere successivamente **ritrasmesso** aumentando così la congestione

Ciò può dipendere da il **throughtput** ossia la **quantità** di dati che possono essere trasmessi attraverso una rete in un determinato **periodo** di tempo.