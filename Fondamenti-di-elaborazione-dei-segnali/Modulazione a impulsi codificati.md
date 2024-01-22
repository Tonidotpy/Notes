---
Created: 2024-01-22 14:19
Author: Antonio Gelain
aliases:
  - PCM
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **modulazione a impulsi codificati** (abbreviato *PCM*) è un metodo di [[Codifica|codifica]] i un [[Segnale|segnale]] analogico ad uno digitale

---

Il codificatore PCM non fa altro che associare una sequenza univoca di $B$ [[Bit|bit]] ad ogni campione, che codificherà quel livello tra i $2^{B}$ possibili

![sistema-PCM](https://www.electroyou.it/fidocad/cache/463c04814c1801b049e0dc41ef6b3fabc4d4e181_3_650.png)

Il [[Bitrate|bitrate]] del PCM, dato un segnale [[Campionamento|campionato]] a $N$ campioni al secondo, in cui ogni campione viene quantizzato su $M$ livelli, risulta essere:
$$r_{b} = N \cdot log_{2} M = N \cdot B\ \left[\frac{bit}{sec}\right]$$
$r_{b}$ è legato alla massima [[Frequenza|frequenza]] del segnale e alla qualità che vogliamo ottenere dopo la [[Quantizzazione|quantizzazione]]
