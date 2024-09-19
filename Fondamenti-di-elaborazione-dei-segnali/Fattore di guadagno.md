---
Created: 2023-09-27 14:19
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Il **fattore di guadagno** è un'operazione che può venire utilizzata su di un [[Segnale|segnale]] che permette di modificarne l'[[Ampiezza|ampiezza]] o la [[Potenza media di un segnale|potenza]]

---

Il guadagno in potenza di un [[Sistema lineare tempo-invariante|sistema LTI]] è pari a:
$$G(f) = |H(f)|^{2}$$

Solitamente il fattore di guadagno viene espresso tramite una **scala logaritmica** (in *dB*):
$$G_{dB}(f) = 10 \log_{10} \left\{\frac{|H(f)|^{2}}{|H(f_{ref})|^{2}}\right\} = 20 \log_{10} \left\{\frac{|H(f)|}{|H(f_{ref})|}\right\}$$
Dove $f_{ref}$ viene spesso scelto come la [[Frequenza di un segnale|frequenza]] correlata al massimo assoluto della [[Risposta in ampiezza|risposta in ampiezza]] del segnale



Se il segnale viene **moltiplicato** per un fattore $k > 1$ si ha un'**amplificazione**
$$kx(t)\ |\ t > 1$$
Se il segnale viene **diviso** per un fattore $k > 1$ si ha un'**attenuazione**
$$kx(t)\ |\ k > 1$$