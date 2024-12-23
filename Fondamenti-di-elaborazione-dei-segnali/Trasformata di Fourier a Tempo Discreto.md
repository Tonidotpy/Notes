---
Created: 2024-10-21 14:46
Author: Antonio Gelain
aliases:
  - DTFT
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **trasformata di Fourier a tempo discreto** (in breve *DTFT*) è una [[Trasformata di Fourier|trasformata]] che, a partire da un segnale discreto $x[n]$, ne fornisce una descrizione periodica del [[Dominio|dominio]] della [[Frequenza|frequenza]].
$$
X(\omega) = \sum\limits_{n=-\infty}^{\infty} x[n] e^{-j \omega n}
$$

---

L'inversa della DTFT è data dalla formula seguente:
$$
x[n] = \frac{1}{2\pi} \int_{-\pi}^{\pi} X(\omega) \cdot e^{j \omega n} d \omega
$$

---

La DTFT è **continua** e **periodica**