---
 Created: 2022-12-21 16:26
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Automatic Repeat Query, ARQ]
 Tags: [protocol]
---

>[!INFO] L'ARQ più che un protocollo è una **classe di protocolli**

**Automatic Repeat reQuest** (*ARQ*) è un metodo di **trasmissione** dei dati che viene utilizzato per garantire l'**affidabilità** della trasmissione in una rete di comunicazione

---

L'ARQ utilizza dei **pacchetti speciali** per notificare il trasmettitore di una avvenuta ricezione corretta (*Acknowledgments* o *ACK*) ^6fb93b

A seconda del protocollo, si possono usare diversi tipi di ACK:
- **ACK individuale**:
	- Indica la ricezione corretta di un pacchetto specifico
	- ACK(n) indica che è stato ricevuto il pacchetto `n`
- **ACK cumulativo**: ^44565d
	- Indica la ricezione corretta di tutti i pacchetti fino a un certo indice
	- ACK(n) indica che sono stati ricevuti tutti i pacchetti fino a quello `n` (**escluso**)
- **ACK negativo (NACK)**
	- Richiede la ritrasmissione di un pacchetto singolo
	- NACK(n) indica che deve essere ritrasmesso il pacchetto `n`
- **Piggybacking**
	- Inserimento di un ACK data in un pacchetto di dati

Alcuni protocolli basati su ARQ sono:
- [[Stop-and-Wait]]
- [[Go-back-N]]
- [[Selective Repeat]]
- [[Transmission Control Protocol|TCP]]
- [[Media Access Control|MAC]]