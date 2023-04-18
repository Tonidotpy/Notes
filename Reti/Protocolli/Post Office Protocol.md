---
 Created: 2022-12-18 19:50
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [POP3]
 Tags: [protocol]
---

**Post Office Protocol** version 3 (*POP3*) è un protocollo di rete utilizzato per **scaricare** i messaggi di **posta elettronica** da un server di posta a un client di posta, come ad esempio Microsoft Outlook o Mozilla Thunderbird

---

La porta utilizzata dal protocollo POP3 è la `110`

POP3 ha due modalità:
1. **Scarica e cancella**: che cancella la email dal server una volta scaricata
2. **Scarica e mantieni**: che copia i messaggi su più client

Si può utilizzare una versione più sicura di POP3 tramite il [[Transport Layer Security|TLS]] utilizzando però la porta `995`