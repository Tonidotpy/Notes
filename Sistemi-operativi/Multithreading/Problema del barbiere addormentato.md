---
 Created: 2023-04-27 10:43
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **problema del barbiere addormentato** è un classico problema che riguarda la [[Sincronizzazione|sincronizzazione]] tra [[Processo|processi]]

---

Si immagini un negozio con un barbiere ed una sedia, ed una stanza di attesa con `n` sedie (`n` può essere `0`).
Le seguenti regole vengono applicate:
- Se non ci sono clienti, il barbiere si addormenta sulla sedia
- Se il barbiere sta dormendo, un cliente deve svegliarlo
- Se un cliente arriva mentre il barbiere sta lavorando, se ne va se tutte le sedie sono occupate, altrimenti si siede nella prima sedia libera
- Quando un barbiere finisce di servire un cliente controlla la stanza di attesa per vedere se ci sono clienti e si addormenta se non ce ne sono

Ci sono due possibili problemi che possono verificasi:
1. Il barbiere si addormenta **mentre** un cliente attende di essere servito
2. Due clienti entrano **contemporaneamente** nel negozio ma trovano un solo posto libero