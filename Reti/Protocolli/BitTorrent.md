---
 Created: 2022-12-19 22:46
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

**BitTorrent** è un protocollo di file sharing **peer-to-peer** che consente di **condividere file** di grandi dimensioni in modo rapido e efficiente

---

Il protocollo BitTorrent prevede:
- Un gruppo di **peer** ossia [[Host|host]] di pari grado che formano un **torrent**
- Un **tracker** ossia un server che tiene traccia dei peer

Il file da inviare viene suddiviso in parti (*chunk*) tipicamente da `256 kB`
Quando un peer entra a far parte del torrent:
- Si **registra** presso il tracker per avere la lista dei peer e si **collega** ad un sottoinsieme di vicini (*neighbors*)
- Inizia ad **accumulare** parti del file col passare del tempo

Mentre effettua il download, il peer carica le sue parti su altri peer
I peer possono entrare e uscire a piacimento dal torrent
Una volta ottenuto l'intero file, il peer può lasciare il torrent **egoisticamente** (*leech*) o rimanere collegato **altruisticamente** (*seeder*)

Per la ricezione delle parti del file si adotta la tecnica del ***rarest first***, dove il peer inizia a scaricare le parti meno disponibile per prime

Durante l'invio vengono valutati ogni 10 secondi i 4 peer vicini che hanno la frequenza di invio più alta (*unchoked peer*) e gli si inviano i propri chunk
Ogni 30 secondi viene selezionato casualmente un altro peer e si inizia ad inviargli delle parti (*optimistically unchoked peer*)
Gli altri peer vengono definiti *choked* e non gli si invia niente

In questo protocollo c'è un sistema di **priorità** (*tit for tat*) dove i peer con un'elevata **frequenza di upload** ricevono più velocemente i file in **download**

---

La ricerca di informazioni può avvenire tramite una ***Distributed Hash Table***, ossia una tabella distribuita su più peer che tiene traccia di dove trovare i file oppure tramite una **directory centralizzata** ossia un server centralizzato che tiene traccia di tutti i peer e dei file che possiedono
Quest'ultimo metodo ha parecchi problemi, quali:
- Unico punto di guasto
- Collo di bottiglia per le prestazioni
- Violazione del diritto d'autore

Per risolvere questi problemi viene utilizzato il ***Query Flooding*** cioé un sistema **completamente distribuito** e di pubblico dominio
Ciascun peer indicizza i file che rende disponibili per la condivisione e nasconde gli altri
Ogni peer cerca di conoscere la **rete di copertura** del torrent cioè la rete formata da tutti i collegamenti logici tra i peer attivi

Per ottimizzare il query flooding viene utilizzata la **copertura gerarchica** dove vengono selezionati dei *peer leader* che tengono traccia dei contenuti propri e dei peer figli