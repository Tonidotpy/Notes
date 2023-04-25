---
 Created: 2023-03-02 08:46
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **processo** è un'entità dinamica caricata nella [[Memoria primaria|memoria primaria]] generata da un [[Programma|programma]]

---

Un processo può essere identificato attraverso un codice univoco chiamato **Process ID** (*PID*) ^c70725

La creazione, distruzione, sospensione e riesumazione, [[Sincronizzazione|sincronizzazione]] e comunicazione dei processi viene gestita interamente dal [[Sistema operativo|SO]]

Un processo in memoria è composta da:
- **Istruzioni** che vengono eseguite in maniera sequenziale
- Una sezione di **[[Dato|dati]] globali**
- Lo [[Stack|stack]] in cui vengono memorizzate le chiamate alle procedure, i loro parametri e le variabili locali
- Lo [[Heap|heap]] utilizzato per l'allocazione dinamica
- Il [[Process Control Block|process control block]]

Un processo può creare un suo **processo figlio** che ottiene le risorse dal SO oppure dal padre stesso (condivisione di risorse)
L'esecuzione tra questi due processi può essere:
- **Sincrona**: il padre attende la terminazione di tutti i suoi figli
- **Asincrona**: avviene un evoluzione *concorrente* tra il padre e i figli

Un processo può terminare in 3 modi:
1. Finisce la sua esecuzione
2. Viene terminato forzatamente dal processo padre
3. Viene terminato forzatamente dal SO

---

Due o più processi possono essere:
- **Indipendenti**: la cui esecuzione è deterministica e riproducibile, e non influenza ne viene influenzata da altri processi
- **Cooperanti**: in cui un processo influenza, o viene influenzato da altri processi e il risultato è variabile e difficilmente riproducibile

La condivisione di informazioni tra più processi cooperanti avviene tramite l'[[Inter-process communication|IPC]]