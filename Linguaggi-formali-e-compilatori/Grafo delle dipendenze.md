---
 Created: 2023-12-31 17:08
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Un **grafo delle dipendenze** è un tipo di [[Grafo|grafo]] utilizzato per valutare se un [[Parse tree annotato|parse tree annotato]] può essere verificato o meno

---

## Costruzione di un grafo delle dipendenze

Per costruire un grafo delle dipendenze per un determinato parse tree annotato bisogna:
- Impostare un nodo del grafo per ogni attributo associato a qualche nodo del parse tree
- Per ogni attributo $X.x$ usato per definire l'attributo $Y.y$, si crea un arco dal nodo di $X.x$ fino al nodo di $Y.y$

Per verificare che il parse tree annotato sia valutabile **deve esistere** un [[Ordinamento topologico|ordinamento topologico]] del grafo delle dipendenze