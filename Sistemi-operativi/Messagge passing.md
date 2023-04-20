---
 Created: 2023-04-20 09:03
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Scambio di messaggi]
 Tags: [IPC]
---

Il **message passing** è una tipologia di [[Inter-process communication|IPC]] che prevede che non ci siano risorse condivise e che tutte le comunicazioni avvengano attraverso l'invio di messaggi tra i [[Processo|processi]]

---

La comunicazione può avvenire in maniera:
- **Diretta**: i processi devono nominarsi esplicitamente
	- **Simmetrica**: viene specificato il processo da cui si riceve il messaggio
	- **Asimmetrica**: il processo mittente riceve tutti i messaggi e li filtra in base al proprio id
- **Indiretta**: i messaggi vengono spediti e ricevuti attraverso delle *mailboxes* (o porte)
  Ogni mailbox ha un proprio id e permette ai processi che la condividono di comunicare tra loro

Lo scambio di messaggi può essere:
- **Bloccante** (o *sincrono*): il mittente blocca l'esecuzione finché il messaggio non è stato ricevuto e il ricevente è bloccato finche non lo riceve
- **Non-bloccante** (o *asincrono*): il mittente invia il messaggio e continua la sua esecuzione mentre il ricevente controlla se è stato ricevuto e procede indipendentemente dal risultato