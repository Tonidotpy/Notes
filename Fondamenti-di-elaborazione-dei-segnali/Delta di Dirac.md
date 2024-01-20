---
Created: 2023-09-27 14:00
Author: Antonio Gelain
aliases:
  - Funzione impulso unitario
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Il **delta di Dirac** (o *funzione impulso unitario*) è una [[Funzione generalizzata|funzione generalizzata]] $\delta(t)$, ovvero una [[Funzione|funzione]] definita unicamente sulla base delle sue proprietà, tale che, data una generica funzione $f(t)$ [[Funzione continua|continua]] e [[Integrale|integrabile]], soddisfa la seguente uguaglianza:
$$\int_{-\infty}^{+\infty} f(t)\delta(t) dt = f(0)$$

---

Si può ottenere una funzione che soddisfi tale proprietà tramite un **passaggio al limite** applicato alla funzione rettangolo di area unitaria

$$\delta(t) = \lim_{T \mapsto 0} \frac{1}{T}\Pi\left(\frac{t}{T}\right) = \begin{cases}
+\infty & t = 0 \\
0 & \text{altrove}
\end{cases}$$
![passaggio-al-limite](https://www.electroyou.it/fidocad/cache/83cf77dd6a4b92f65c8316781ca3af34ccd7f142_3.png)

>[!INFO] Il delta di Dirac viene generalmente rappresentato tramite una **freccia**

![rappresentazione-delta-di-dirac](https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Dirac_distribution_PDF.png/310px-Dirac_distribution_PDF.png)