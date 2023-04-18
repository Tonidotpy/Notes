---
 Created: 2022-12-26 16:40
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Loopback]
 Tags: []
---

Un **indirizzo di loopback** è un [[Indirizzo IPv4|indirizzo IP]] che viene utilizzato per **inviare** un pacchetto di dati a **se stesso** sulla stessa macchina o sullo stesso dispositivo di rete

---

L'IP riservato a questo scopo è `127.0.0.0/8` (`::1/128` per [[Indirizzo IPv6|IPv6]]) ma viene generalemente utilizzato `127.0.0.1` anche se l'**HostID** è irrilevante

Viene usato per **testare** le applicazioni di rete simulando una connessione tra due dispositivi utilizzandone uno solo
I pacchetti non lasciano mai veramente il dispositivo