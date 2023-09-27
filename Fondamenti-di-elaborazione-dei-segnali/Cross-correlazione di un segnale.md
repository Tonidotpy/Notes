---
Created: 2023-09-27 15:11
Author: Antonio Gelain
aliases:
  - Correlazione incrociata di un segnale
tags:
---

La **cross-correlazione di un segnale** (o *correlazione incrociata*) tra due segnali $x(t)$ e $y(t)$ è definita per [[Energia di un segnale|segnali di energia]] come:
$$\mathcal{R}_{xy}(\tau) = \int_{-\infty}^{+\infty} x(t) y(t + \tau) dt$$
ed è definita per [[Potenza media di un segnale|segnali di potenza]] come:
$$\mathcal{R}_{xy}(\tau) = \lim_{T \mapsto \infty} \frac{1}{T} \int_{\frac{-T}{2}}^{\frac{T}{2}} x(t) y(t + \tau) dt$$

---

La cross-correlazione permette di rilevare **pattern simili** presenti in segnali diversi oltre che per rilevare ritardi tra segnali simili