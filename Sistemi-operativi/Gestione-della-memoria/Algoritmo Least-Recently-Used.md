---
 Created: 2023-05-13 14:21
 Author: Antonio Gelain
 Aliases: [Algoritmo LRU]
 Tags: [gestione-della-memoria]
---

L'**algoritmo Least Recently Used** (o *algoritmo LRU*) è un [[Algoritmo|algoritmo]] per la sostituzione delle [[Paginazione|pagine]] nel caso di [[Page fault|page fault]], che seleziona le pagine che sono rimaste inutilizzate per più tempo

---

Questo tipo di algoritmo si può implementare in diversi modi:
- Tramite **timestamp** che viene associato ad ogni pagina e aggiornato ogni volta che la pagina viene referenziata
  In caso di page fault viene sostituita la pagina col timestamp **minore**
- Tramite [[Pila|stack]] in cui vengono memorizzati i numeri delle pagine e vengono spostati verso la cima ogni volta che le pagine corrispondenti vengono referenziate
  In caso di page fault viene sostituita la pagina referenziata nel **fondo** dello stack
- Tramite dei [[Bit|bit]] di riferimento che vengono associati ad ogni pagina ed aggiornati ad ogni riferimento (nel caso di più bit viene usato un [[Registro di scorrimento|registro di scorrimento]])
  Nel caso di page fault viene sostituita la pagina col bit di riferimento a `0` (nel caso di un singolo bit) oppure col valore del **registro di scorrimento** più alto (nel caso di più bit)