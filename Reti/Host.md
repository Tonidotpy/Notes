---
 Created: 2022-12-08 15:39
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **host** è un [[Computer|computer]] o un altro dispositivo connesso a una [[Rete|rete]] che è in grado di fornire servizi attraverso dei [[Reti/Processo|processi]].

---

## Architetture degli host

### Client/Server

In questa architettura un **host** funge da **server** e fornisce servizi ad uno o più host chiamati **client** che a loro volta li richiedono.

Questo tipo di architettura è **fortemenete centralizzata** e permette un'ottima **gestione della rete** e della **protezione dei dati**.
Ovviamente il **carico** dalla parte del server è di gran lunga maggiore di quello del client.

Tipici esempi di architetture **client/server** sono:
- i **browser** che richiedono pagine web ai **server**
- i **client/server email**

![client-server|300](https://intellipaat.com/blog/wp-content/uploads/2021/09/image-99.png)

Tra il server e il client si può **interfacciare** un [[Server proxy|proxy]] che fa da **tramite** per le richieste e risposte tra i due host

### Peer to Peer (P2P)

In questa architettura tutti gli **host** vengono trattati come **pari grado** (*peer* appunto) condividendo fra loro le risorse.

Questo tipo di architettura è **fortemenete distribuita** e viene utilizzata principalmente per la **condivisione di file** e la **distribuzione di contenuti** su larga scala.
Tuttavia ciò rende più difficile la gestione della rete e la protezione dei dati.

Tipici esempi di architetture **P2P** sono:
- qualsiasi client [[BitTorrent]]

![p2p|300](http://webmasterblog.altervista.org/wp-content/uploads/2017/10/p2p.png)

### Ibridi

Questa architettura **combina** le caratteristiche dei modelli client/server e P2P in cui gli host possono agire sia come **client** che come **server** a seconda delle esigenze

Alcuni esempi di architetture **ibride** sono:
- **Skype**
- **Messaggistica instantanea**