---
 Created: 2022-12-29 20:09
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [CSMA]
 Tags: []
---

Il **Carrier Sense Multiple Access** (*CSMA*) è un metodo di **accesso** al mezzo di trasmissione che viene utilizzato in alcune reti di comunicazione per **gestire** l'accesso al mezzo di trasmissione da parte di più dispositivi

---

Il CSMA **controlla** se il canale di trasmissione è libero prima di **inviare** messaggi, nel caso in cui sia occupato ritarda la trasmissione

Esistono diverse versioni del CSMA basate sulla **persistenza**:
- **Non-persistente** (*0-persistente*): se il canale è occupato attende un tempo **casuale** e molto più lungo del tempo di trasmissione prima della ritrasmissione
- **1-persistente**: se il canale è occupato attende finché non si libera, dopodiché trasmette **subito** e se si verifica una collisione, il nodo attende un tempo casuale e ritenta la procedura ^08bf26
- **p-persitente**: se il canale è occupato attende finché non si libera, dopodiché con **probabilità** `p` trasmette il frame altrimenti attende un tempo casuale e molto più lungo del tempo di trasmissione per ritentare (anche nel caso in cui si verifichi una collisione)  ^fffc51

Il **periodo di vulnerabilità** dipende dal tempo di **propagazione** $\tau$ e dal tempo richiesto per **rilevare** se il canale è occupato $T_{a}$, perciò $T_{v} = \tau + T_{a}$
In generale, CSMA si utilizza quando $\tau << T$ (tempo di trasmissione)

Anche con il CSMA ci possono essere delle **collisioni**, in quel caso si spreca l'intero tempo di trasmissione