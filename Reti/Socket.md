---
 Created: 2022-12-17 19:05
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **socket** è un endpoint di **comunicazione** utilizzato per **inviare** e **ricevere** dati attraverso una [[Rete|rete di computer]]

---

Ogni [[Processo|processo]] può utilizzare un socket come *"porta"* per **comunicare** con altri **processi** su [[Host|host]] diversi

Ad un socket è associato il numero della **porta** che utilizza per la comunicazione
La porta è un numero a `16 bit` (da 0 a 65535) e può essere classificata come:
- **Statica** (o *well-known*): è minore di 1024 e viene utilizzata dai protocolli standard
- **Dinamica** (o *ephimeral*): viene assegnata automaticamente dal [[Sistema operativo|SO]] quando si apre una connessione