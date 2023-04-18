---
 Created: 2022-12-29 16:24
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Redundancy Check]
 Tags: []
---

Il **controllo tramite ridondanza** è un metodo utilizzato per verificare la **correttezza** dei dati trasmessi o memorizzati in un sistema di elaborazione

---

Per poter controllare un messaggio tramite ridondanza il suo contenuto deve essere inviato **più volte**
Più messaggi uguali vengono inviati **minore** sarà la probabilità che un errore non venga trovato però **maggiore** sarà il numero di dati da inviare e perciò anche il tempo di invio del messaggio

Una tecnica detta ***interleaving***, che consiste nel riordino dei bit, viene utilizzata come protezione contro le **raffiche di errori**

Ad esempio:
- Messaggio: HELLO
- Ridondanza: HHH EEE LLL LLL OOO
- Interleaving: HEL LOH ELL OHE LLO
- Raffica di errori: HEL LOH EXX XXX LLO
- De-interleaving: HHX EEX LXL LXL OXO
- Scelta a maggioranza: HELLO