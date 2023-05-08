---
 Created: 2023-05-08 11:09
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

Una **partizione fissa** è una [[Sistemi-operativi/Gestione-della-memoria/Partizione|partizione]] la cui dimensione è stata definita a priori

---

L'assegnazione della [[Memoria primaria|memoria]] per i [[Processo|processi]] viene gestita dall [[Scheduling|scheduling]] a lungo termine in due possibili modi:
1. Tramite una [[Coda|coda]] **singola**:
   La coda viene gestita tramite [[First Come First Served|FCFS]], o tramite **scansione** della coda
2. Assegnando una coda per **partizione**:
   Un processo viene assegnato alla partizione più piccola che può contenerlo
   
Questa tipologia di partizionamento della memoria è molto semplice ma è soggetta al problema della [[Frammentazione|frammentazione]]