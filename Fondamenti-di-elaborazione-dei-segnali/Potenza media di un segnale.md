---
Created: 2023-09-27 15:00
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **potenza media di un segnale** $x(t)$ viene definita come:
$$P_{x} = \lim_{T \mapsto \infty} \frac{1}{T} \int_{\frac{-T}{2}}^{\frac{+T}{2}} x^{2}(t) dt\ \ \text{[Watt]}$$
che coincide col [[Valore quadratico medio di un segnale|valore quadratico medio]]

---

La potenza media di un segnale viene utilizzata laddove l'[[Energia di un segnale|energia]] non può essere calcolata

>[!ATTENTION] I segnali di potenza hanno **sempre** energia infinita

---

Nel dominio discreto la potenza può essere calcolata nel seguente modo:
$$P_{x} = \lim_{K \rightarrow \infty} \frac{1}{K} \sum\limits_{k = - \frac{K}{2}}^{\frac{K}{2}} x^{2}[k]\ \ P_{x} \ne 0$$
