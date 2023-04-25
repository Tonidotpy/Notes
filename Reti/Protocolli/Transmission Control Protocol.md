---
 Created: 2022-12-21 17:41
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [TCP]
 Tags: [protocol]
---

Il **Transmission Control Protocol** (*TCP*) è un protocollo di rete a livello di trasporto utilizzato per garantire la **trasmissione affidabile** dei dati su una rete

---

TCP e un protocollo che utilizza [[Pipelining|pipelining]]

Il TCP è un protocollo di tipo **punto-punto**, ossia prevede un mittente e un destinatario
Vengono utilizzati dei meccanismi di [[Controllo di flusso|controllo di flusso]] e di [[Controllo della congestione|congestione]] che deifiniscono la dimensione delle finistre che sono **dinamiche** sia per il mittente che per il destinatario
Il TCP utilizza [[Automatic Repeat reQuest#^44565d|ACK cumulativi]]

Il flusso di dati è affidabile, consegnato in ordine e *full-duplex* ossia un flusso bidirezionale sulla stessa connessione

É un protocollo **orientato alla connessione** che viene avviata tramite scambio di messaggi di controllo (*handshaking*) e terminata nello stessa maniera (*tear-down*)

---

## Datagramma TCP

![TCP-datagram](https://www.gatevidyalay.com/wp-content/uploads/2018/09/TCP-Header-Format.png)

Il campo di **flag** è formato da.
- **URG**: da priorità a questo pacchetto rispetto agli altri che non hanno questa flag settata (generalmente non utilizzato)
- **ACK**: segnala che il numero di riscontro è valido
- **PSH**: invia subito il messaggio (generalmente non utilizzato)
- **RST**: richiede il reset immediato della connessione
- **SYN**: richiede l'inizio della [[Sincronizzazione|sincronizzazione]] per stabilire una connessione
- **FIN**: richiede il termine della connessione

Il campo **Window Size** indica il numero di byte che il ricevitore può immagazzinare e di conseguenza rappresenta anche la massima quantità di dati in transito durante un [[Round Trip Time|RTT]]

I segmenti TCP hanno un tempo massimo per ricevere una risposta chiamato [[Retransmission TimeOut|RTO]]

Il protocollo TCP lavora per byte e cerca di inviare segmenti il cui ***payload*** ha lunghezza al più quanto il **Maximum Segment Size** (*MSS*)
L'MSS dipende dall'[[Internet Protocol versione 4#^e2d109|MTU]] del livello sottostante  

## Connessione TCP

La sincronizzazione per la connessione tra due host avviene tramite un ***three-way handshake***
All'inizio della connessione un host `A` invia un segmento con flag **SYN** settata a `1`
Un altro host `B` riceve il messaggio e a sua volta ne invia uno con flag **SYN** e **ACK** a `1`
L'host `A` riceve il messaggio e invia un segmento con **ACK** a `1` iniziando così la comunicazione

Per terminare la comunicazione l'host `A` invia un segmento con flag **FIN** a `1`
L'host `B` riceve il messaggio e invia un segmento con flag **FIN** e **ACK** a `1` chiudendo a metà la connessione (*half-closed*)
L'host `B` una volta terminato di inviare tutti i dati invia un messaggio con flag **FIN** a `1`
L'host `A` chiude definitivamente la connessione inviando un segmento con flag **FIN** e **ACK** a `1`

Alternativamente può essere richiesta una chiusura *"brusca"* della connessione tramite la flag **RST** che viene inviata direttamente senza attenderne la risposta