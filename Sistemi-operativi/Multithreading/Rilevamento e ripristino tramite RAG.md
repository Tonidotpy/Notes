---
 Created: 2023-05-05 13:41
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading]
---

Il **rilevamento e rispristino tramite [[Resource Allocation Graph|RAG]]** è un [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]] che permette di risolvere il problema dei [[Deadlock|deadlock]]

---

>[!WARNING] Funziona solamente con una risorsa per tipo

In questo algoritmo il **grafo di attesa** viene analizzato periodicamente per verificare se esistono deadlock e nel caso in cui ne venga rilevato uno iniziano la fase di **ripristino**