---
 Created: 2023-05-08 12:57
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

La tecnica del **buddy system** permette di ridurre il problema della [[Frammentazione|frammentazione]] della [[Memoria|memoria]]

---

La memoria viene vista come una [[Lista|lista]] di blocchi di dimensione $2^{k}$
Quando viene richiesta una certa dimensione $s$, si cerca un blocco libero con dimensione "adatta" purché sia una potenza di 2

Quando un blocco viene **rilasciato** se si formano due blocchi liberi adiacenti di dimensione $2^{k}$ è possibile [[Compattazione|compattarli]] ottenendo un unico blocco di dimensione $2^{k+1}$