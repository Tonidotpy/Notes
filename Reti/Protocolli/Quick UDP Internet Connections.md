---
 Created: 2022-12-23 16:46
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [QUIC]
 Tags: [protocol]
---

**Quick UDP Internet Connections** (*QUIC*) è un protocollo di rete basato su [[User Datagram Protocol|UDP]] sviluppato da Google per **migliorare** la velocità e l'efficienza del trasferimento dei dati su Internet

---

QUIC è stato progettato per:
- **Evitare** fenomeni di *Head-of-Line blocking*
- **Ridurre** la latenza rispetto alle connessioni [[Transmission Control Protocol|TCP]]

Può essere implementato a [[Livello di applicazione|livello applicativo]] anziché nel kernel

Molte connessioni [[HyperText Transfer Protocol|HTTP]] richiedono [[Transport Layer Security|TLS]] per funzioni di sicurezza ma in QUIC lo **scambio delle chiavi** viene incorporato nel processo di *handshake* iniziale in modo da eliminare la necessità di negoziare il protocollo di sicurezza **dopo** aver impostato la connessione

Nel caso di un evento di cambio della rete QUIC **include** un ID di connessione al server che non dipende dalla fonte o dalla rete usata
Si può così ristabilire la connessione inviando nuovamente un pacchetto contenente tale ID