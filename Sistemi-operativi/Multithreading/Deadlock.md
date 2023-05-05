---
 Created: 2023-04-25 16:00
 Author: Antonio Gelain
 Aliases: [Stallo]
 Tags: [multithreading]
---

Il **deadlock** (o *stallo*) indica una situazione in cui due o più [[Processo|processi]] si **bloccano** a vicenda **attendendo** che uno esegua una certa azione che serve all'altro e viceversa

---

Le condizioni necessarie per cui si verifichi un deadlock sono:
- La **mutua esclusione**: almeno una risorsa deve essere non condivisibile
- **Hold and wait**: deve esistere un processo che detiene una risorsa e che attende di acquisirne un'altra
- Nessuna [[Prelazione|prelazione]]: le risorse non possono essere rilasciate se non *volontariamente* dal processo che le usa
- **Attesa circolare**: deve esistere un [[Insiemi|insieme]] di processi che attendono **ciclicamente** il liberarsi della risorsa
Per far si che il deadlock si verifichi tutte le precedenti condizioni devono verificarsi **contemporaneamente**

Un modello utile per capire se possono verificarsi dei deadlock è il [[Resource Allocation Graph|RAG]]

---

Esistono diverse soluzioni che permettono di gestire un deadlock:
- [[Prevenzione statica]]
- [[Prevenzione dinamica]]
- [[Rilevamento e Ripristino|Rilevamento e ripristino]]
- **Algoritmo dell struzzo**, ossia ignorare del tutto il problema dal momento che i deadlock si verificano raramente e la loro risoluzione è molto costosa