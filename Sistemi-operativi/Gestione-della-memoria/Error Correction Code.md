---
 Created: 2023-06-15 15:03
 Author: Antonio Gelain
 Aliases: [ECC]
 Tags: [gestione-della-memoria]
---

L'**error correction code** (o *ECC*) permette di capire se un [[Disco rigido#^3700c3|settore]] di un [[Disco rigido|disco fisso]] contiene dati corretti o meno

---

Durante un'operazione sui dati di un settore viene calcolato l'ECC che se non combacia con quello memorizzato risulta in un errore (*bad block*)

La gestione dei bad block può avvenire:
- **Off-line**: memorizzando i settori corrotti in una lista
- **On-line**: il controllore mappa i settori corrotti su nuovi settori funzionanti non utilizzati

