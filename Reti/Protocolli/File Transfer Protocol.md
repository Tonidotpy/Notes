---
 Created: 2022-12-18 19:27
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [FTP]
 Tags: [protocol]
---

**File Transfer Protocol** (*FTP*) è un protocollo di **rete** utilizzato per trasferire **file** da un [[Computer|computer]] a un altro su una rete, come ad esempio Internet

---

La porta utilizzata dal protocollo FTP è la `21`

Chi richiede una connessione tramite FTP deve prima ottenere l'**autorizzazione** sulla connessione di controllo che una volta concessa gli permette di cambiare la directory remota inviando dei **comandi**

Quando viene ricevuto un comando per **trasferire** un file il server apre una **connessione** col client che chiude solo al termine del trasferimento