---
 Created: 2022-12-21 16:45
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

l protocollo **Go-back-N** è un tipo di protocollo di **trasmissione** dei dati che viene utilizzato per garantire l'**affidabilità** della trasmissione in una rete di comunicazione

---

Go-back-N è un protocollo che utilizza il [[Pipelining|pipelining]]

Il mittente può avere fino a `N` pacchetti senza ACK in pipeline e ha un **timer** per il più vecchio pacchetto senza ACK
Se il timer scade, ritrasmette tutti i pacchetti presenti nella [[Finestra di trasmissione|finestra di trasmissione]]
Il ricevente invia solo [[Automatic Repeat reQuest#^44565d|ACK cumulativi]]