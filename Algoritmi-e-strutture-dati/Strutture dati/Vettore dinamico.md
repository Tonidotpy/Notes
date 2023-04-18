---
 Created: 2023-01-14 18:20
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **vettore dinamico** è una [[Sequenza|sequenza]] **omogenea** di elementi di qualsiasi tipo

---

La [[Complessità temporale|complessità]] dell'**inserimento** di un elemento è $O(1)$ nel caso ottimo (ossia l'inserimento alla fine del vettore) e $O(n)$ nel **caso pessimo** (ossia l'inserimento all'inizio del vettore)
Valgono le stesse complessità per la **rimozione** di un elemento

Nel caso venga inserito un nuovo elemento e non ci sia spazio nel contenitore **raddoppiarne** la capacità risulta in una [[Analisi ammortizzata|complessità ammortizzata]] di $O(1)$