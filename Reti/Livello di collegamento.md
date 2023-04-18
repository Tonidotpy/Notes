---
 Created: 2022-12-29 15:58
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Livello di Data Link]
 Tags: []
---

Il **livello di collegamento** è uno dei livelli del modello [[Pila ISO-OSI|OSI]] che si occupa della **trasmissione** dei dati sulla **rete fisica** e di garantirne la **corretta** ricezione

---

In questo livello vengono:
- **Rilevati** e **corretti** errori sui dati
- **Condivisi** i canali di tipo *broadcast* e accesso multiplo
- **Indirizzati** i dati a livello di data link

Il livello di *data link* fornisce sevizi di:
- **Creazione** di un frame di livello 2 che fornice un meccanismo di accesso al canale se il [[Mezzo di comunicazione fisico|mezzo di comuncazione]] è condiviso con altri dispositivi e utilizza indirizzi di livello 2 chamati [[Indirizzo MAC|MAC]]
- **Consegna affidabile** tra nodi adiacenti
- **Controllo di flusso** adattando la velocità di trasmissione
- **Rilevamento** di errori
- **Correzzione** degli errori riducendo il numero di ritrasmissioni
- **Half-duplex** e **Full-duplex**

---

Il controllo degli errori avviene tramite:
- [[Controllo di parità]]
- [[Controllo tramite ridondanza]]
- [[Cyclic Redundancy Check|CRC]]