---
 Created: 2023-05-04 11:29
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading, algoritmo]
---

L'**algoritmo del banchiere** è un [[Algoritmo|algoritmo]] utilizzato per risolvere il problema dei [[Deadlock|deadlock]]

---

>[!INFO] Questo algoritmo funziona anche con più istanze di risorse

L'idea è che i [[Processo|processi]] vengano visti come dei clienti che possono richiedere **credito** presso la banca (fino ad un certo limite) e le risorse allocabili sono viste come il **denaro**
É chiaro che la banca, non può permettere a tutti i clienti di raggiungere il loro limite di credito contemporaneamente

L'algoritmo è costituito da:
1. Un algoritmo i **allocazione**
2. Un algoritmo di **verifica dello [[Stato|stato]]**

Ogni volta che un processo richiede una risorsa si determina se soddisfarla ci lascia in uno stato *safe*