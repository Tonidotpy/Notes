---
 Created: 2022-12-17 21:17
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [HTTP,HTTP/2.0, HTTP/2]
 Tags: [protocol]
---

Come per [[HyperText Transfer Protocol|HTTP]], la sua **versione 2.0** è un protocollo di trasmissione di dati utilizzato su Internet per lo scambio di risorse web come pagine HTML, immagini e video

---

**HTTP 2.0** introduce alcune importanti **novità** rispetto alla versione precedente di HTTP, come ad esempio il supporto per le **connessioni multiple** e le **richieste multiple** su una singola connessione, il supporto per l'**encoding** delle risposte del server e il supporto per l'uso di *header compression*

Questo nuovo tipo di protocollo è focalizzato sulle **prestazioni** e più nello specifico sulla **latenza** percepita dall'utente e l'utilizzo delle **risorse** di rete e dei server

HTTP/2 si basa su [[SPDY]], un [[Protocollo|protocollo]] utilizzato per trasportare contenuti sul web con **minima latenza** tramite:
- **Multiplexing di flussi**: supporta un numero limitato di flussi su una singola connessione [[Transmission Control Protocol|TCP]]
- **Priorità delle richieste**: il client può inviare quante richieste desidera, assegnando a ciascuna una priorità
- **Compressione dell'header**: diminuisce i *byte* trasmessi

---

In HTTP/2 viene aggiunto un nuovo **framing binario**, responsabile della modalità di incapsulamento e trasferimento dei messggi.
La **semantica** del messaggio HTTP rimane **invariata** ma cambia la **codifica** in transito
Tutte le comunicazioni HTTP/2 sono suddivise in messaggi e frame più **piccoli**, ognuno codificato in formato **binario**

Tutte le comunicazioni vengono eseguite all'interno di una **singola connessione** [[Transmission Control Protocol|TCP]] che può portare qualsiasi numero di stream **bidirezionali** di byte
Ogni stream ha un **identificativo univoco** e le informazioni di **priorità** opzionali
Ogni messaggio consiste in uno o più **frame** che è la più piccola unità di comunicazione che porta un tipo specifico di dati
I frame di diversi stream possono essere **interposti** e quindi **riassemblati** tramite l'**identificatore di flusso** incorporato nell'intestazione

Nella nuova versione di HTTP gli stream hanno un **peso** e una **dipendenza** associati
I pesi vanno da 1 (più **leggero**) a $2^{8}$ = 256 (più **pesante**)

Tutte le connessioni HTTP/2 sono **persistenti** in quanto si rende necessaria solo una connessione per origine e il multiplexing può avvenire all'interno di essa