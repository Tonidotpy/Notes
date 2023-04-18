---
 Created: 2022-12-10 19:00
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **livello di applicazione** è il livello più alto della struttura di rete del [[Pila ISO-OSI|modello OSI]] (*Open Systems Interconnection*),, e [[Pila TCP-IP|TCP-IP]] che definisce le **regole** per lo **scambio di dati** tra sistemi informatici in una rete

---

Il livello di applicazione si occupa delle attività di comunicazione che sono specifiche per l'**applicazione** che si sta utilizzando, come ad esempio l'invio di una richiesta di ricerca su un motore di ricerca o l'invio di un messaggio di posta elettronica

In questo livello sono presenti [[Protocollo|protocolli]] di **pubblico dominio** come *HTTP* e *SMTP* oppure **proprietari** come quelli di *Skype*

Alcuni esempi di protocolli utilizzati sono i seguenti:
- [[HyperText Transfer Protocol|HTTP]]
- [[Simple Mail Transfer Protocol|SMTP]]
- [[Post Office Protocol|POP3]]
- [[Internet Message Access Protocol|IMAP]]
- [[File Transfer Protocol|FTP]]
- [[Domain Name System|DNS]]
- [[Telnet]]
- [[Session Initiation Protocol|SIP]]
- [[Real-time Transport Protocol|RTP]]

Alcune loro applicazioni sono le seguenti:

| Applicazione               | Protocollo |
| -------------------------- | ---------- |
| Posta elettronica          | SMTP       |
| Accesso a terminali remoti | Telnet     |
| Web                        | HTTP       |
| Trasferimento file         | FTP        |
| Multimedia in streaming    | HTTP, RTP  |
| Telefonia Internet         | SIP, RTP   |

Per la distribuzione di contenuti multimediali una [[Content Delivery Network|CDN]] rappresenta una soluzione comune