---
 Created: 2023-05-04 10:18
 Author: Antonio Gelain
 Aliases: []
 Tags: [multithreading]
---

La **prevenzione statica** è un metodo utililzzato per risolvere il problema dei [[Deadlock|deadlock]] cercando di **impedire** che si verifichi una delle 4 condizioni necessarie affinche lo stallo avvenga

---

Per quanto riguarda la **mutua eclusione** non si può fare molto

Per l'**hold and wait** un [[Processo|processo]] può allocare all'inizio tutte le risorse che deve utilizzare e non può ottenere risorse se non ne ha già altre
Questo metodo ha un **basso utilizzo** delle risorse e può causare [[Starvation|starvation]]

Nel caso della "**non [[Prelazione|prelazione]]**" un processo che richiede una risorsa disponibile deve prima cedere tutte le altre risorse che detiene, oppure può cedere risorse su richiesta di altri processi
Il problema di questo metodo è che può essere utilizzato solo per risorse il cui stato può essere facilmente "**ristabilito**"

Per quanto riguarda l'**attesa circolare** si può assegnare una **priorità** ad ogni risorsa, cosicché i processi possano richiedere risorse solamente in **ordine crescente** di priorità