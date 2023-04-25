---
 Created: 2023-04-25 14:40
 Author: Antonio Gelain
 Aliases: [Regione critica]
 Tags: [multithreading]
---

Una **sezione critica** (o *regione critica*) è una porzione di un [[Programma|programma]] che accede ad una risorsa **condivisa** tra più [[Processo|processi]]

---

La soluzione al problema delle sezioni critiche deve rispettare 3 criteri:
1. **Mutua esclusione**: solo un processo alla volta può accedera a quella sezione
2. **Progresso**: solo i processi che **stanno per entrare** nella sezione possono decidere chi entra e la decisione non può essere mandata all'infinito
3. **Attesa limitata**: deve esistere un limite per il numero di volte per cui un processo può attendere di seguito

Possono esistere diverse soluzioni suddivise in due categorie:
1. [[Sofware]]
	- [[Algoritmo del fornaio]]
	 - [[Semafori]]
2. [[Hardware]]
	- [[Test and Set]]
	- [[Compare and Swap]]