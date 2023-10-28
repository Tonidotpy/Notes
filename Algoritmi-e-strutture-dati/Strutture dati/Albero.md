---
 Created: 2023-01-14 18:48
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Albero radicato]
 Tags: [data_structure]
---

Un **albero** è una [[Struttura di dati|struttura dati]] formata da un [[Algoritmi-e-strutture-dati/Strutture dati/Insieme|insieme]] finito di **nodi** e un insieme di [[Coppia|coppie]] di nodi chiamati **vertici** tali che:
- Esiste un nodo designato come nodo **radice**
- Ogni nodo, esclusa la radice, ha esattamente un **arco entrante**
- Esiste un [[Cammino|cammino]] **unico** dalla radice ad ogni nodo
- L'albero è **connesso**

---

## Definizioni

 - **Radice**: un nodo appartenente ad un albero senza vertici entranti
 - **Foglia**: un nodo appartenente ad un albero senza vertici uscenti
 - **Nodo interno**: un nodo che non sia ne foglia ne radice
 - **Profondità**: la lunghezza del cammino semplice dalla radice al nodo (misurato in numero di archi)
 - **Livello**: l'insieme di nodi alla stessa profondità
 - **Altezza**: la profondità massima delle foglie di un albero
 - **Fratello**: un nodo appartenente allo stesso livello di un altro
 - **Figlio**: un nodo $B$ connesso ad un nodo $A$ tale che $B$ si trova nel livello immediatamente successivo di $A$
 - **Padre**: il nodo $A$ direttamente connesso ad un nodo $B$ tale che $A$ si trova nel livello immediatamente precedente a quello di $B$
 - **Sottoalbero**: l'insieme di nodi tali da formare un albero, connessi ad un nodo padre
 - **Ramo**: l'insieme dei nodi appartenenti ad un cammino dalla radice ad una foglia di un albero
 - **Successore**: dato un nodo $A$ in un albero, il nodo il cui valore è il minor valore possibile maggiore di $A$