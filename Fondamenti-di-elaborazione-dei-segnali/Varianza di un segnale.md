---
Created: 2023-09-27 14:52
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---


La **varianza di un segnale** è data dalla seguente formula:
$$\sigma^{2}_{x} = \overline{x^{2}} - \overline{x}^{2} = \lim_{T \mapsto \infty} \frac{1}{T} \int_{\frac{-T}{2}}^{\frac{T}{2}} (x(t) - \overline{x})^{2}dt$$

---

La varianza esprime l'**intensità** della variazione del segnale, più un segnale varia maggiore sarà la sua varianza

---

Nel dominio discreto la varianza può essere calcolata nel seguente modo:
$$\sigma_{x}^{2} = \lim_{K \rightarrow \infty} \frac{1}{K} \sum\limits_{k = - \frac{K}{2}}^{\frac{K}{2}} [x[n] - \bar{x}]^{2}$$
