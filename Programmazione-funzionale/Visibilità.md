---
 Created: 2022-06-16 14:59
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Visibilità
La **visibilità** è la possibilità di richiamare un [[Nomi|nome]] in un determinato punto di un programma.

La **visibilità** può essere:
- **statica**: un [[Nomi|nome]] non locale può essere richiamato nel [[Blocchi|blocco]] che lo include,
  può essere implementata tramite:
	- *catena statica*: una sequenza di chiamate a *runtime*;
	- *schermo*: un array che rappresenta la catena statica ma permette di accedere all'*i*-esimo elemento con un costo **costante**;
- **dinamica**: un [[Nomi|nome]] non locale può essere richimato nel [[Blocchi|blocco]] in cui è stato attivato più di recente,
  può essere implementato tramite:
	- *A-list*: le associazioni vengono memorizzate in uno stack ad accesso lineare;
	- *Tabella centrale dell'[[Ambienti|ambiente]]*: una tabella che memorizza tutti i [[Nomi|nomi]] in un programma a cui vengono associate delle liste di associazioni ad accesso costante;