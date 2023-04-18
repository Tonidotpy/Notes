---
 Created: 2022-06-18 12:35
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Garbage collection
Un **garbage collector** è un software che si occupa di **deallocare** periodicamente la memoria che non viene più utilizzata dal programma.

L'utente può allocare memoria ma non deallocarla.
Viene utilizzata per risolvere problemi del tipo:
- *tombstones*: quando un oggetto fa riferimento ad uno spazio di memoria non più valido (deallocato);
- quando uno spazio di memoria viene allocato ma non esiste alcun oggetto cui fa riferimento e risulta quindi impossibile deallocarlo (spreco di memoria).

Un **garbage collector** può essere implementato tramite:
- **
- *contatore di riferimenti*: si tiene traccia del numero di riferimenti per ogni area di memoria e quando il contatore scende a zero questa viene deallocata.
  In caso di strutture circolari è possibile mantenere lo spazio allocato quando in realtà non ho alcun riferimento esplicito a tale spazio di memoria;
- *segna e spazza*: inizialmente segna tutti gli oggetti come non utilizzati, successivamente controlla ogni riferimento e marca l'oggetto puntato come utilizzato, infine recupera tutta la memoria inutilizzata.
  Questo procedimento può impattare gravemente sulle prestazioni di un programma.