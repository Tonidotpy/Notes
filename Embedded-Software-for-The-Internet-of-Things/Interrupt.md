---
 Created: 2023-09-26 19:41
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **interrupt** è un evento che notifica la [[Central Process Unit|CPU]] quando un'operazione di [[Input Output|I/O]] è terminata, in questo modo il [[Processore|processore]] è in grado di eseguire il proprio programma senza dover controllare attivamente lo stato delle periferiche

---

Una volta ricevuta una richiesta di interrupt la CPU blocca l'esecuzione del codice corrente ed esegue il cosiddetto **interrupt handler** ossia una [[Funzione|funzione]] che permette di gestire la richiesta di interrupt

Dato che spesso accade che più dispositivi facciano partire un interrupt vi si può assegnare una **priorità** e si può specificare al dispositivo un suo gestore di interrupt

Per gestire tutti i vari interrupt viene utilizzato un [[Programmable Interrupt Controller|PIC]] che si interfaccia tra i dispositivi e la CPU