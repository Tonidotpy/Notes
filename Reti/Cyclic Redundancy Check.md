---
 Created: 2022-12-29 16:40
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [CRC]
 Tags: []
---

Il **Cyclic Redundancy Check** (*CRC*) è un metodo utilizzato per verificare la **correttezza** dei dati trasmessi o memorizzati in un sistema di elaborazione

---

Il CRC è un algoritmo più efficente per il rilevamento degli errori

Considera i bit di dati come un **numero binario** `D` e sceglie una sequenza di `r+1 bit` (detta **generatore**) e un numero `G` (noto sia al mittente che al ricevente)
L'obiettivo è **comporre** il CRC (`R`) scegliendo `r bit` in modo che:
1. I dati `D` siano esattamente **divisibili** per `G` (modulo 2) con resto `R`
2. La divisione di `<D,R>` per `G` dia resto `0` (altrimenti c'è un errore)
3. Il numero di bit in caso di *errori a raffica* sia minore di `r`
La coppia `<D,R>` viene calcolata come $<D,R> = (D \cdot 2^{r}) \text{ XOR } R$
