---
 Created: 2023-10-11 14:28
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **trasformata di Fourier** è un'operazione che associa a una [[Funzione|funzione]] i valori dei **coefficienti** di quest sviluppi lineari, dandone in questo modo una rappresentazione nel [[Spettro di un segnale periodico|dominio delle frequenze]]
$$W(f) = \int_{-\infty}^{+\infty} w(t) e^{-j2\pi ft} dt$$

---

La trasformata di Fourier inversa è data dalla formula seguente:
$$w(t) = \int_{-\infty}^{+\infty} X(f) e^{j2\pi ft} df$$

## Trasformate notevoli

### Rettangolo

L'integrale di Fourier nel caso di una funzione rettangolo è il seguente:
$$x(t) = V_{0}\Pi\left(\frac{t}{T}\right) \rightarrow X(f) = \int_{-\frac{T}{2}}^{\frac{T}{2}} V_{0} e^{-2\pi jft} dt = \frac{V_{0}}{2\pi jf}[e^{\pi jfT} - e^{-\pi jfT}] = V_{0}T \frac{\sin{(\pi fT)}}{\pi fT} = V_{0}T \text{sinc}(fT)$$