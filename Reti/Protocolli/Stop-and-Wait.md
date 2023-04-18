---
 Created: 2022-12-21 16:36
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

Il protocollo **Stop-and-Wait** è un tipo di protocollo di **trasmissione** dei dati che viene utilizzato per garantire l'**affidabilità** della trasmissione in una rete di comunicazione

---

Il trasmettitore invia una [[Protocollo#^b551b1|PDU]] (e ne mantiene una copia in locale) e imposta un **timeout**
Attende la ricezione del rispettivo **ACK** e:
- Se non riceve alcun ACK entro il timeout reinvia la **stessa PDU**
- Se lo riceve:
	- Controlla che l'ACK non contenga errori
	- Controlla il numero di sequenza
	- Se tutto è OK invia la **PDU successiva**

Il ricevitore:
- Controlla se ci sono errori
- Controlla il numero di sequenza:
	- Se è corretto e in ordine, invia l'ACK e passa l'[[Protocollo#^b551b1|SDU]] ai layer superiori
	- Se ci sono errori cancella la PDU