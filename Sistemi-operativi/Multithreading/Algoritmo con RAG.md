---
 Created: 2023-05-04 10:47
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading, algoritmo]
---

L'**algoritmo con RAG** è un tipo di [[Algoritmo|algoritmo]] che utilizza un [[Resource Allocation Graph|RAG]] modificato per risolvere il problema dei [[Deadlock|deadlock]]

---

>[!WARNING] Questo algoritmo funziona solo se si ha un'istanza per ogni risorsa

Il RAG viene esteso con archi di *rivendicazione*, ossia degli archi da un [[Processo|processo]]  $P_{i}$ ad una risorsa $R_{j}$ tale che $P_{i}$ può richiedere $R_{j}$ in futuro, e vengono indicati con una freccia trattegiata

All'inizio, ogni processo deve dire quali risorse vorrebbe usare durante la sua esecuzione e la richiesta viene siddisfatta se l'allocazione della risorsa non crea un [[Ciclo|ciclo]] nel RAG