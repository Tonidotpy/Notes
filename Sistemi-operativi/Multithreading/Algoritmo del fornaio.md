---
 Created: 2023-04-25 15:11
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading]
---

L'**[[Algoritmo|algoritmo]] del fornaio** è uno dei metodi di **mutua esclusione** che permettono l'esecuzione delle [[Sezione critica|sezioni critiche]] da parte di più [[Processo|processi]] **concorrenti**

---

L'algoritmo è il seguente:
1. Ogni processo sceglie un **numero casuale**
2. Il processo avente il **numero minore** viene servito per primo
3. Se due o più processi hanno scelto lo **stesso numero** si da la precedenza al processo con l'**[[Processo#^c70725|ID]] minore