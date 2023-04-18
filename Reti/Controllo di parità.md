---
 Created: 2022-12-29 16:12
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **controllo di parità** è un metodo utilizzato per **verificare** la correttezza dei dati trasmessi o memorizzati in un sistema di elaborazione

---

Un singolo bit può rilevare **singoli errori** attraverso uno dei due possibili metodi:
- **Even parity**: dove il bit di parità controlla che il numero di bit a `1` presenti nel messaggio sia **pari**
- **Odd parity**: dove il bit di parità controlla che il numero di bit a `1` presenti nel messaggio sia **dispari**

Si può applicare la parità dei bit anche su **2 dimensioni** suddividendo il messaggio in **righe multiple** di lunghezza fissa e controllandone la parità per ogni riga e colonna
Questo permette di poter identificare anche la **posizione** di dove è avvenuto il singolo errore

>[!WARNING] Il controllo di parità non è affidabile al 100%