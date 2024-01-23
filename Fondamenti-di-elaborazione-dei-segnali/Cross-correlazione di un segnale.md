---
Created: 2023-09-27 15:11
Author: Antonio Gelain
aliases:
  - Correlazione incrociata di un segnale
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **cross-correlazione di un segnale** (o *correlazione incrociata*) tra due segnali $x(t)$ e $y(t)$ è definita per [[Energia di un segnale|segnali di energia]] come:
$$\mathcal{R}_{xy}(\tau) = \int_{-\infty}^{+\infty} x(t) y(t + \tau) dt$$
ed è definita per [[Potenza media di un segnale|segnali di potenza]] come:
$$\mathcal{R}_{xy}(\tau) = \lim_{T \mapsto \infty} \frac{1}{T} \int_{\frac{-T}{2}}^{\frac{T}{2}} x(t) y(t + \tau) dt$$

---

La cross-correlazione permette di rilevare **pattern simili** presenti in segnali diversi oltre che per rilevare ritardi tra segnali simili

---

Nel dominio discreto la cross-correlazione può essere calcolata per segnali di energia come:
$$\mathcal{R}_{xy}(k) = \sum\limits_{n = -\infty}^{\infty} x[n] y[n + k]$$
mentre per segnali di potenza come:
$$\mathcal{R}_{xy}(k) = \lim_{K \rightarrow \infty} \frac{1}{K} \sum\limits_{n = - \frac{K}{2}}^{\frac{K}{2}} x[n] y[n + k]$$
