---
Created: 2023-09-28 10:07
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---
L'**integrale di convoluzione** è una formula che rappresenta l'**uscita** (esatta) di un [[Sistema lineare tempo-invariante|sistema LTI]] ad un generico ingresso $x(t)$
> $$\lim_{\Delta t \mapsto 0} y_{R}(t) = \int_{-\infty}^{+\infty} x(\tau) h(t - \tau) d\tau = y(t) = x(t) \cdot h(t)$$

---

Nel dominio discreto la convoluzione viene calcolata tramite una [[Addizione|sommatoria]]:
$$y[n] = \sum\limits_{k = -\infty}^{+\infty} x[k]h[n - k]$$
La [[Serie|sequenza]] $h[n]$ prende anche il nome di **kernel** o **maschera di convoluzione**
