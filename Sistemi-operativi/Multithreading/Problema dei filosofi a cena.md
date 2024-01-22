---
 Created: 2023-04-25 16:18
 Author: Antonio Gelain
 Aliases: [Problema dei cinque filosofi]
 Tags: [multithreading]
---

Il **problema dei filosofi a cena** (o *problema dei cinque filosofi*) è un esempio che illustra un comune problema di **controllo della [[Concorrenza|concorrenza]]** fra [[Processo|processi]]

---

![problema-dei-filosofi-a-cena|400](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7b/An_illustration_of_the_dining_philosophers_problem.png/800px-An_illustration_of_the_dining_philosophers_problem.png)

Il problema pone cinque filosofi seduti attorno ad un tavolo, ognuno con del cibo ed una forchetta alla sua destra.
Un filosofo passa tutto il suo tempo a periodi alternati fra pensare e mangiare, e per mangiare necessita di due forchette che può prendere solo una alla volta.
Una volta terminato di mangiare il filosofo riappoggia le forchette sul tavolo e ricomincia a pensare.
Il problema consiste nello sviluppo di un [[Algoritmi-e-strutture-dati/Algoritmo|algoritmo]] che impediscal lo [[Deadlock|stallo]] o la morte per [[Starvation|inedia]]

Lo **stallo** può verificarsi se ogni filosofo prende la forchetta alla sua destra (o sinistra) e deve attendere che il filosofo alla sua sinistra (o destra) abbia finito di mangiare per ottenere la seconda forchetta; questo implica che un filosofo per **iniziare** a mangiare deve **finire** di mangiare il che è impossibile

La situazione di **indedia** può verificarsi indipendentemente dallo stallo quando un filosofo non riesce mai ad ottenere entrambe le forchette per poter mangiare
