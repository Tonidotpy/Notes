---
 Created: 2023-04-21 11:27
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [scheduling]
---

Il **dispatcher** è un modulo del [[Sistema operativo|SO]] che passa effettivamente il controllo della [[CPU]] ai [[Processo|processi]] scelti dallo [[Scheduler#^7fc376|scheduler a breve termine]]

---

Il tempo necessario al dispatcher per fermare un processo e farne ripartire un altro è detto **latenza di dispatch** e deve essere il più bassa possibile

Un possibile modello di dispatcher è quello a **cicli di burst** ossia l'altrernanza ciclica tra sequenze di CPU e sequenze di [[Input Output|I/O]]