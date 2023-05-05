---
 Created: 2023-05-04 10:29
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading]
---

La **prevenzione dinamica** è una tecnica per la risoluzione dei [[Deadlock|deadlock]] che tenta di analizzare e prevenire gli stalli in base alle richieste delle risorse da parte dei [[Processo|processi]]

---

Lo [[Stato|stato]] di assegnazione delle risorse viene calcolato come:
- Numero di istanze disponibili e allocate
- Richieste massime dei processi

Il sistema si trova in uno **stato sicuro** (*safe*) se esiste una **[[Sequenza|sequenza]] sicura**, ovvero se usando le risorse disponibili, può allocare risorse ad ogni processo in modo che ciascuno di essi possa terminare la sua esecuzione

Una **sequenza** di procesi ($P_{1}, ..., P_{n}$) è *safe* se, per ogni processo $P_{i}$, le risorse che può richiedere possono essere esaudite usando:
- Le risorse **disponibili**
- Le risorse **detenute** dal processo $P_{j}\ |\ j < i$ (attendento che $P_{j}$ termini)
Se non esiste una tale sequenza allora siamo in uno stato **non sicuro** (*unsafe*), che non necessariamente significa che siamo in uno stato di deadlock, ma che potrebbe verificarsene uno

---

Esistono due [[Algoritmo|algoritmi]] che permettono di mantenere i processi in uno stato *safe*:
1. L'[[Algoritmo con RAG|algoritmo con RAG]]
2. L'[[Algoritmo del banchiere|algoritmo del banchiere]]