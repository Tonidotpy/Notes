---
 Created: 2022-12-26 16:35
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Indirizzo di trasmissione limitata]
 Tags: []
---

Un **indirizzo di trasmissione limitata** (*Limited Broadcast Address*) è un [[Indirizzo IPv4|indirizzo IP]] che viene utilizzato per **inviare** un pacchetto di dati a **tutti** i dispositivi di rete in una specifica [[Local Area Network|LAN]]

---

Questo tipo di indirizzo si ottiene impostando tutti e 32 i bit a `1` ottenendo così `255.255.255.255`
I datagrammi inviati a questo indirizzo non escono **mai** dalla rete locale

Viene utilizzato quando un dispositivo deve capire in che rete si trova