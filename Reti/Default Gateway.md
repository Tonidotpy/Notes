---
 Created: 2022-12-26 15:48
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **Default Gateway** è un [[Indirizzo IPv4|indirizzo IP]] che viene utilizzato per **instradare** i pacchetti di dati verso altre reti quando non è possibile trovare un percorso specifico nella [[Tabella di Routing|tabella di routing]]

---

Per gli [[Host|host]] si tratta di solito dell'indirizzo IP del [[Router|router]]
Per i router invece viene utilizzato `0.0.0.0/0` come indirizzo IP collegato ad un'interfaccia di rete che si suppone sappia come **inoltrare** ulteriormente il messaggio