---
 Created: 2022-12-18 19:54
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [IMAP]
 Tags: [protocol]
---

**Internet Message Access Protocol** (*IMAP*) è un protocollo di rete utilizzato per **gestire** la **posta elettronica** su un server

---

La porta utilizzata da IMAP è la `143`

A differenza del protocollo [[Post Office Protocol|POP3]], IMAP è più **complesso**, mantiene i messaggi nel server e consente di **organizzarli** in cartelle
IMAP conserva anche lo **stato** dell'utente tra le varie sessioni

Si può utilizzare una versione più sicura di IMAP tramite il [[Transport Layer Security|TLS]] utilizzando però la porta `993`