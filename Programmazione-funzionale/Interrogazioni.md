---
 Created: 2022-06-18 13:55
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Interrogazioni
Un'**interrogazione** (o *query*) permette di trovare per quali valori un predicato è **vero**.

Le principali strategie per implementare le **query** sono:
- *forward chaining*: si inizia da una clausola esistente e si cerca di derivare il [[Programmazione logica|goal]] ;
- *backward chaining*: si inizia dal [[Programmazione logica|goal]] e si cerca di lavorare a ritroso.