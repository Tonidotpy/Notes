---
 Created: 2022-06-16 20:36
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Stack
Uno **stack** è un'area di memoria di tipo LIFO (*last in first out*) in cui possono essere allocate:
- variabili globali;
- variabili locali di sottoprogrammi in assenza di ricorsione;
- costanti determinate a runtime;
- tabelle utilizzate in fase di esecuzione.

Per ogni instanza di un sottoprogramma salviamo nello **stack** un [[Record di attivazione|record di attivazione]] (o *frame*) che ne contiene le informazioni.
