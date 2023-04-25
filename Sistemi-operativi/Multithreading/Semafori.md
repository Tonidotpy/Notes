---
 Created: 2023-04-25 15:30
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading]
---

Un **semaforo** è un tipo di [[Astrazione dei dati|tipo di dato astratto]] gestito da un [[Sistema operativo|sistema operativo]] per gestire la [[Sincronizzazione|sincronizzazione]] tra [[Processo|processi]]

---

Un semaforo `S` offre due [[Primitiva|primitive]] [[Operazione atomica|atomiche]]:
1. **Signal** `V(s)`: incrementa il valore `S` di `1`
2. **Wait** `P(s)`: tenta di decrementare il valore di `S` di `1` se questo non è `0`

Esistono due tipi di **[[Implementazione|implementazione]] concettuali** di semafori:
1. **Binari**: che possono assumere come valori solamente `0` oppure `1`
2. **Generici**: che possono assumere qualsiasi valore [[Numeri naturali|intero non negativo]]

Sono possibili due diversi tipi di **implementazioni reali** di semafori:
1. Con **busy waiting** (tramite *spinlock*): la [[Central Process Unit|CPU]] controlla attivamente il verificarsi della condizione di accesso alla [[Sezione critica|sezione critica]]
2. Con **sleep** (tramite *[[Mutex|mutex]]*): il processo viene messo in **attesa** che si verifichi la condizione di accesso alla sezione critica

---

L'utilizzo dei semafori può causare alcuni problemi quali:
- [[Deadlock]]
- [[Starvation]]
- [[Problema del produttore-consumatore]]
- [[Problema dei filosofi a cena]]
- [[Problema del barbiere addormentato]]