---
 Created: 2022-12-17 21:06
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **proxy** è un server che funge da **intermediario** per le **richieste** da parte dei client di risorse presenti in altri server

---

Un proxy viene utilizzato per **alleggerire** il carico di **richieste** al **server** tramite il *caching*
Più **client** inviano richieste al proxy che **risponde** al posto del server se possibile, altrimenti manda una **richiesta** al server e ne **inoltra** la risposta ai client

Questo procedimento può portare a un problema di **sincronizzazione** tra il proxy e il server che può essere risolto inviando una richiesta al server specificando la **data** della copia dell'oggetto, il server risponderà alla **cache** informandola se l'oggetto é o non é stato **modificato**