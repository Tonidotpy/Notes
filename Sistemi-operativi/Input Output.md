---
Created: 2023-04-14 15:08
Author: Antonio Gelain
aliases:
  - I/O
tags:
---

Con **input/output** (*I/O*) si intendono tutte le interfaccie informatiche messe a disposizione da un [[Sistema operativo|SO]] ai [[Programma|programmi]] per effettuare un cambio o svincolo di [[Dato|dati]] o segnali

---

Il SO nasconde all'utente le specifiche caratteristiche dei dispositivi di I/O

Un dispositivo di input/output si può astrarre pensandolo come un meccanismo che si interfaccia con l'esterno tramite due tipi di [[Registro|registri]]:
1. Lo **status register** che contiene le [[Informazione|informazioni]] riguardo il dispositivo, come ad esempio l'ID del dispositivo, il produttore, ecc...
2. Il **data register** che contiene i valori che possono essere letti o scritti da o verso il dispositivo

Esistono due metodi per accedere a tali registri:
- Tramite [[Primitiva|primitive]] di **I/O** che permetto due operazioni:
    1. **Input**: i [[Dato|dati]] vengono letti dal dispositivo
    2. **Output**: i dati vengono scritti nel dispositivo
- Tramite [[Indirizzo di memoria|indirizzi di memoria]] riservati, i cosiddetti **memory-mapped I/O**