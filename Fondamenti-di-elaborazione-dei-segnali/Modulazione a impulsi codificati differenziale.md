---
Created: 2024-01-23 11:24
Author: Antonio Gelain
aliases:
  - DPCM
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **modulazione a impulsi codificati differenziale** è un metodo differenziale di [[Codifica|codifica]] dei [[Segnale|segnali]]

---

>[!INFO] Le prestazioni del codificatore DPCM dipendono dalle caratteristiche del segnale

La DPCM realizza una **predizione** del campione successivo (che può essere anche basata sui campioni precedenti) e poi se ne codifica la differenza tra il campione corrente e la predizione (*errore di predizione*)
$$\hat{x}_{i} = a_{1}\tilde{x}_{i-1} + ... + a_{n}\tilde{x}_{i - n}$$

Con opportuni meccanismi (ad esempio la *codifica entropica*) è possibile risparmiare [[Bit|bit]]
Inoltre il [[Bitrate|bitrate]] **non è fisso** e dipende da quanto il segnale è correlato e quindi predicibile e da quale livello di errore possiamo tollerare
