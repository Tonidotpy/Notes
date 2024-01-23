---
Created: 2023-09-27 15:23
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

L'**autocorrelazione di un segnale** è un caso particolare di [[Cross-correlazione di un segnale|cross-correlazione]] in cui un [[Segnale|segnale]] $x(t)$ viene messo in correlazione con se stesso

---

$\mathcal{R}_{x}(\tau)$ assume sempre il valore massimo per $\tau = 0$ dato che il segnale è identico a se stesso
Perciò si ha:
- Per [[Potenza media di un segnale|segnali di potenza]] $\mathcal{R}_{x}(0) = \overline{x^{2}}$ ossia il [[Valore quadratico medio di un segnale|valore quadratico medio]]
- Per [[Energia di un segnale|segnali di energia]] $\mathcal{R}_{x}(0) = E_{x}$ ossia il valore dell'energia

La velocità con cui l'autocorrelazione scende rispetto al picco è una misura della *memoria* del segnale, ossia di quanto il segnale è prevedibile sulla base dell'andamento precedente

---

Nel dominio discreto l'autocorrelazione può essere calcolata per segnali di energia come:
$$\mathcal{R}_{x}(k) = \sum\limits_{n = -\infty}^{\infty} x[n] x[n + k]$$
mentre per segnali di potenza come:
$$\mathcal{R}_{x}(k) = \lim_{K \rightarrow \infty} \frac{1}{K} \sum\limits_{n = - \frac{K}{2}}^{\frac{K}{2}} x[n] x[n + k]$$
