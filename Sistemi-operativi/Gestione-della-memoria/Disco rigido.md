---
 Created: 2023-06-15 13:54
 Author: Antonio Gelain
 Aliases: [Disco fisso, Hard Disk, HDD]
 Tags: [gestione-della-memoria]
---

Un **disco rigido** (o *disco fisso*) è un dispositivo di [[Memoria secondaria|memoria di massa]] di tipo **magnetico** che utilizza uno o più dischi magnetizzati per l'archiviazione dei [[Dato|dati]]

---

Un disco rigido è formato da: ^ce3209
- Una o più **testine** che permettono di leggere o scrivere sul disco ^dde93b
- Una o più **superfici**, detti anche *platter* (ossa più dischi magnetici impilati)
- Delle **traccie** (*track*): anelli concentrici facenti parte della superficie
- Un **cilindro** (*cylinder*): l'insieme delle tracce di tutte le superfici alla stessa distanza dal centro
- Dei **settori** (*sector*): una sezione (o spicchio) di una singola traccia (o dell'intero piatto) ^3700c3
- Dei **cluster**: insieme di settori contigui

![disco-rigio](https://www.irecoverydata.com/wp-content/uploads/2016/05/parti-hdd.png)

---

Il **tempo di accesso** di un disco rigido dipende da:
- **Seek time**: il tempo necessario per spostare la testina sulla traccia ^5df52d
- **Latency time**: il tempo necessario a posizionare il settore sotto la testina
- **Transfer time**: il tempo necessario al settore per passare sotto la testina

Per minimizzare il tempo medio di accesso al disco vengono utilizzati vari [[Algoritmi-e-strutture-dati/Algoritmo|algoritmi]] di [[Scheduling|scheduling]]:
- [[First Come First Served|FCFS]]
- [[Shortest Seek Time First|SSTF]]
- [[SCAN]]
- [[CSCAN]]
- [[LOOK]]
- [[CLOOK]]
- [[N-step SCAN]]

---

Per gestire i blocchi di memoria difettosi viene utilizzato l'[[Error Correction Code|ECC]]
