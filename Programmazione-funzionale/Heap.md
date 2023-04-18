---
 Created: 2022-06-16 20:37
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Heap
L'**heap** è una regione di memoria in cui [[Blocchi|blocchi]] possono essere allocati e deallocati arbitrariamente.

L'**heap** può essere formato da:
- blocchi di **grandezza fissa** collegati tra loro in modo da formare una '*free list*'.
  Ad ogni allocazione richiesta viene cercato un blocco appropriato:
	- *first fit*: il primo blocco grande abbastanza,
	  più veloce ma utilizza peggio la memoria;
	- *best fit*: il più piccolo blocco grande abbastanza,
	  più lento ma usa meglio la memoria;
- blocchi di **grandezza variabile**

Le operazione in un **heap** devono:
- essere **efficienti**;
- evitare di **sprecare memoria**:
	- *frammentazione interna*:
		- Un blocco di spazio $Y > X$ viene allocato;
		- Viene sprecato $Y - X$ spazio;
	- *frammentazione esterna*:
		- Lo spazio richiesto è presente però non è utilizzabile in quanto è frammentato in pezzi troppo piccoli;

La gestione dell'**heap** può avvenire con:
- una singola lista: l'allocazione è lineare;
- con liste multiple: la divisione dei blocchi tra le liste può essere:
	- *statico*;
	- *dinamico*.
