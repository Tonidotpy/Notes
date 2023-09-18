---
 Created: 2023-09-15 09:23
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **albero di derivazione** è un [[Albero|albero]]  la cui radice contiene lo *starting point* e per ogni passo di [[Derivazione|derivazione]] si generano $n$ figli del nodo la cui derivazione è messa in atto

---

Esempio:
$$S \rightarrow aSb\ |\ \epsilon$$
```mermaid
graph TD;
	S-->a
	S-->S2
	S-->b
	S2-->a2
	S2-->b2
```