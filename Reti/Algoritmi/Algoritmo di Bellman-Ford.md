---
 Created: 2022-12-28 16:45
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Bellman-Ford]
 Tags: [algorithm]
---

L'**algoritmo di Bellman-Ford** è un algoritmo di **ricerca di percorsi** che viene utilizzato per trovare il percorso **più breve** tra due nodi in un grafo

---

Bellman-Ford è un **algoritmo distribuito** e non richiede la conoscenza della topologia della rete

Richiede che ogni nodo nella rete conosca:
- I propri **vicini**
- Il **costo** del link verso i vicini

Quando il costo di un link cambia se **aumenta** gli aggiornamenti avvengono più **lentamente** rispetto a se **diminuisce**

Di seguito una rappresentazione dell'algoritmo in pseudocodice:

```python
def bellman_ford(graph, source, destination):
  # Inizializza la distanza di ogni nodo dalla sorgente a infinito
  distance = {}
  for node in graph:
    distance[node] = INF
  distance[source] = 0

  # Esegui il relaxamento di tutti gli archi del grafo per V-1 volte
  for i in range(len(graph) - 1):
    # Per ogni arco del grafo
    for u, v, w in graph.edges():
      # Se la distanza del nodo v è maggiore della distanza del nodo u più il peso dell'arco (u, v), aggiorna la distanza di v
      if distance[v] > distance[u] + w:
        distance[v] = distance[u] + w

  # Verifica se esistono cicli negativi nel grafo
  for u, v, w in graph.edges():
    if distance[v] > distance[u] + w:
      return False, {}

  # Restituisci la distanza del nodo destinazione dalla sorgente e la mappa delle distanze
  return True, distance[destination], distance
```

---

L'algoritmo di Bellman-Ford ha un problema denominato ***Count-to-Infinity*** che si tratta di una **situazione** in cui due o più [[Router]] si aggiornano a vincenda **molto lentamente** fino a raggiungere il percorso minimo effettivo nella rete
Esistono varie soluzioni per questo problema:
- **Massimo numero di hop** (15 hop): riduce il tempo di convergenza
- **Split horizon**: è una soluzione semplice che omette le rotte apprese da un vicino di un nodo aggiornato
- **Poisoned reverse**: finché un nodo $x$ raggiunge un nodo $z$ attraverso $y$, $x$ comunica ad $y$ che la sua distanza da $z$ è **infinito**

Non è detto che *split horizon* e *poisoned reverse* funzionino sempre