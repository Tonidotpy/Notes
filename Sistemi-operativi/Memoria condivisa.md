---
 Created: 2023-04-20 09:12
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [IPC]
---

La **memoria condivisa** è un modello di [[Inter-process communication|IPC]] dove vi è una regione di [[Memoria primaria|memoria]] accessibile da più [[Processo|processi]] contemporaneamente, con lo scopo di fornire un mezzo di comunicazione

---

Per utilizzare la memoria condivisa un processo deve crearla se non esiste e aggiungerla al proprio spazio di indirizzi
Una volta compiute tutte le operazioni di scrittura e lettura il processo rimuove il segmento di memoria condivisa

Un altro metodo per la comunicazione a memoria condivisa è attraverso le [[Pipe|pipe]] che agiscono come **condotti** tra due processi
Le pipe si suddividono in:
- **Pipe ordinarie**: il mittente scrive ad una estremità della pipe mentre il destinatario legge all'altra estremità; la pipe è perciò **unidirezionale**
- **Pipe con nome**: questo tipo di pipe sono **bidirezionali** è sono più potenti delle pipe ordinarie
  Più processi possono usare la stessa pipe e non c'è alcuna relazione padre-figlio tra i processi