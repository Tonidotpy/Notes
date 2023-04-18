---
 Created: 2022-12-18 19:37
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [SMTP]
 Tags: [protocol]
---

**Simple Mail Transfer Protocol** (*SMTP*) è un protocollo di rete utilizzato per inviare **e-mail** da un [[Computer|computer]] a un altro su una rete, come ad esempio Internet

---

Il protocollo SMTP utilizza la porta `25`

Con questo protocollo avviene un **trasferimento diretto** dal server trasmittente al ricevente tramite una connessione persistente che avviene in **tre** fasi:
1. ***Handshaking***
2. **Trasferimento** di messaggi
3. **Chiusura**

I **comandi** inviati sono formati da del semplice **testo** mentre le **risposte** sono formate da **codici** di stato ed **espressioni**

Un **messaggio** SMTP deve essere nel formato **ASCII** a `7 bit` e la sua **fine** deve essere determinata dai caratteri `<CR><LF>.<CR><LF>` (*`\r\n.\r\n`*)

Alcune righe aggiuntive nell'**intestazione** del messaggio possono specificare che il contenuto è di tipo **MIME** (*Multipurpose Internet Mail Extensions*) ossia un file **multimediale** codificato in *base 64*

Si può utilizzare una versione più sicura dell'SMTP tramite il [[Transport Layer Security|TLS]] utilizzando però la porta `465`