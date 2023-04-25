---
 Created: 2023-04-25 16:03
 Author: Antonio Gelain
 Aliases: [Problema del buffer limitato]
 Tags: [multithreading]
---

Il **problema del produttore-consumatore** (o *problema del [[Buffer|buffer]] limitato*) è un esempio classi di [[Sincronizzazione|sincronizzazione]] tra [[Processo|processi]]

---

Il problema descrive due processi, uno *produttore* ed uno *consumatore* che condividono un **buffer** di dimensione fissata.
Il produttore **genera** [[Dato|dati]] e li deposita nel buffer di continuo.
**Contemporaneamente** il consumatore **consuma** i dati prodotti prelevandoli dal buffer.
Il problema è assicurare che il produttore non elabori nuovi dati se il buffer è **pieno** e che il consumatore non cerchi dati se il buffer è **vuoto**