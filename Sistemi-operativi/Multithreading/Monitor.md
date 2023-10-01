---
 Created: 2023-04-29 15:00
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading]
---

Un **monitor** è una [[Struttura di dati|struttura dati]] che permette la [[Sincronizzazione|sincronizzazione]] tra [[Processo|processi]]

---

> [!INFO] All'interno di un monitor viene **eseguito** solamente un processo alla volta

Il monitor contiene delle [[Variabile|variabili]] che possono essere modificate solamente attraverso le [[Funzione|funzioni]] `wait` e `signal` definite dal monitor stesso

La funzione `wait` **blocca** il processo chiamante mentre la funzione `signal` sveglia **esattamente** un processo sceltro dallo [[Scheduler|scheduler]]
Al termine del esecuzione del  `signal` il processo che l'ha invocato viene **bloccato** e ne viene sbloccato un altro oppure il processo **esce** dal monitor 