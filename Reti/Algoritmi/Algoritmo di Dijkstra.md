---
 Created: 2022-12-28 15:21
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Dijkstra]
 Tags: [algoritmo]
---

L'**algoritmo di Dijkstra** è un algoritmo di **ricerca** di percorsi che viene utilizzato per trovare il percorso **più breve** tra due nodi in un grafo

---

Si assume che la **topologia** della rete e tutti **costi** dei link siano noti

>[!INFO] L'algoritmo di Dijkstra funziona **solo** se tutti i costi hanno un valore maggiore o uguale a `0`

La [[Complessità temporale|complessità]] dell'algoritmo con una rete di `n` nodi è di $O(n^{2})$ in quanto ad ogni iterazione bisogna controllare tutti i nodi $w \notin P$ dove `P` è una **coda con priorità**

Di seguito viene fornita un'implementazione in pseudocodice:

```python
def dijkstra(graph, source, destination):
  # Inizializza la distanza di ogni nodo dalla sorgente a infinito
  distance = {}
  for node in graph:
    distance[node] = INF
  distance[source] = 0

  # Inizializza la coda di priorità per i nodi non ancora visitati
  queue = PriorityQueue()
  queue.put(source, 0)

  # Finché ci sono nodi non ancora visitati
  while not queue.empty():
    # Estrai il nodo con la distanza minima dalla coda di priorità
    current_node = queue.get()

    # Se il nodo corrente è la destinazione, interrompi l'algoritmo
    if current_node == destination:
      break

    # Per ogni nodo adiacente al nodo corrente
    for neighbor in graph[current_node]:
      # Calcola la distanza del nodo adiacente dalla sorgente attraverso il nodo corrente
      new_distance = distance[current_node] + graph[current_node][neighbor]

      # Se la distanza calcolata è minore della distanza attuale del nodo adiacente, aggiornala
      if new_distance < distance[neighbor]:
        distance[neighbor] = new_distance

        # Aggiungi il nodo adiacente alla coda di priorità
        queue.put(neighbor, new_distance)

  # Restituisci la distanza del nodo destinazione dalla sorgente
  return distance[destination]
```