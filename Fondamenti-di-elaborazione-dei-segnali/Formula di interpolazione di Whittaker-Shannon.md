---
 Created: 2024-09-19 12:39
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **formula di interpolazione di Whittaker-Shannon** è un metodo utilizzato per ricostruire [[Segnale|segnali]] a tempo continuo e [[Banda|banda]] limitata da una serie di [[Campionamento|campioni]] equidistanti

$$x(t) = \text{sinc}(f_{c} t) \sum\limits_{n = -\infty}^{+\infty} x_{n} \delta(t - nT_{c}) = \sum\limits_{n = -\infty}^{+\infty} x_{n}\text{sinc}(f_{c}t) \cdot \delta(t - nT_{c}) = \sum\limits_{n = -\infty}^{+\infty} x_{n} \text{sinc}(f_{c}(t - nT_{c})) = \sum\limits_{n = -\infty}^{+\infty} x_{n} \text{sinc}(f_{c}t - n)$$

---

>[!IMPORTANT] La ricostruzione del segnale non presenta [[Aliasing di un segnale|aliasing]] solamente se $T_{c} \le \frac{1}{2 f_{max}}$

<p><a href="https://commons.wikimedia.org/wiki/File:Nyquist_sampling.gif#/media/File:Nyquist_sampling.gif"><img src="https://upload.wikimedia.org/wikipedia/commons/4/43/Nyquist_sampling.gif" alt="Nyquist sampling.gif" height="189" width="576"></a></p>
