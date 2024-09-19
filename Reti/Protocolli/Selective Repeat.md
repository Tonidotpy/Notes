---
Created: 2022-12-21 16:35
Author: Antonio Gelain
aliases: 
tags:
  - protocol
---

Il protocollo **Selective Repeat** è un tipo di protocollo di **trasmissione** dei dati utilizzato per trasmettere pacchetti di dati su una rete

---

Selective Repeat e un protocollo che utilizza [[Pipelining|pipelining]]

Il mittente può avere fino a `N` pacchetti senza ACK in pipeline e mantiene un **timer** per ciascun pacchetto che non l'ha ricevuto
Quando il timer scade, ritrasmette solo i pacchetti che non hanno avuto ACK
Il ricevente dà gli ACK solo ai singoli pacchetti