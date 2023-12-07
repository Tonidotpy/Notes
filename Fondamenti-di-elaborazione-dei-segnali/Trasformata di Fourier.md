---
 Created: 2023-10-11 14:28
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **trasformata di Fourier** è un'operazione che associa a una [[Funzione|funzione]] i valori dei **coefficienti** di questi sviluppi lineari, dandone in questo modo una rappresentazione nel [[Spettro di un segnale periodico|dominio delle frequenze]]
$$W(f) = \int_{-\infty}^{+\infty} w(t) e^{-j2\pi ft} dt$$

---

La trasformata di Fourier inversa è data dalla formula seguente:
$$w(t) = \int_{-\infty}^{+\infty} W(f) e^{j2\pi ft} df$$

## Trasformate notevoli

### Rettangolo

L'integrale di Fourier nel caso di una funzione rettangolo è il seguente:
$$x(t) = V_{0}\Pi\left(\frac{t}{T}\right) \rightarrow X(f) = \int_{-\frac{T}{2}}^{\frac{T}{2}} V_{0} e^{-2\pi jft} dt = \frac{V_{0}}{2\pi jf}[e^{\pi jfT} - e^{-\pi jfT}] = V_{0}T \frac{\sin{(\pi fT)}}{\pi fT} = V_{0}T \text{sinc}(fT)$$

### Costante

Si può ottenere la trasformata di una funzione costante prendendo la funzione rettangolare e portando $T$ a infinito:
$$x(t) = V_{0}\Pi\left(\frac{t}{T}\right) \rightarrow X(f) = V_{0}T\text{sinc}(fT) \Rightarrow \lim_{T \mapsto +\infty} V_{0} \Pi \left(\frac{t}{T}\right) \equiv V_{0} \rightarrow V_{0}\delta(f)$$

### Esponenziale

Un'altra trasformata comune è quella dell'esponenziale causale:
$$\mathfrak{F}\{ e^{-\alpha t} \cdot 1(t) \} = \int_{0}^{+\infty} e^{-\alpha t} \cdot e^{-j2\pi ft} dt = \int_{0}^{+\infty} e^{-(\alpha + j2\pi f)t} dt = - \frac{e^{-(\alpha + j2 \pi f)t} \big|_{0}^{+\infty}}{\alpha + j2\pi f} = \frac{1}{\alpha + j2\pi f}$$

### Sinusoidi

Anche i segnali sinusoidali sono molto comuni e la loro trasformata è particolarmente semplice:
$$
\begin{matrix}
x(t) = \cos(2\pi f_{0}t) \leftrightarrow X(f) = \frac{1}{2}[\delta(f + f_{0}) + \delta(f - f_{0})] \\
x(t) = \sin(2\pi f_{0}t) \leftrightarrow X(f) = \frac{j}{2}[\delta(f + f_{0}) + \delta(f - f_{0})]
\end{matrix}
$$

## Proprietà

### Simmetria Hermitiana

La trasformata di Fourier gode della [[Simmetria Hermitiana|simmetria Hermitiana]]

$$x(t) \in \mathbb{R} \Rightarrow X(f) = X^{*}(-f)$$

>[!ATTENTION] Questa proprietà vale solo per segnali reali


### Simmetria nel tempo

Se un segnale reale è pari la sua trasformata è **puramente reale**, altrimenti se è dispari è **puramente immaginaria**

$$
\begin{matrix}
x(t) \in \mathbb{R} \text{ pari} & \Rightarrow & X(f) = 2\int_{0}^{+\infty} x(t)\cos(2\pi ft) dt \\
x(t) \in \mathbb{R} \text{ dispari} & \Rightarrow & X(f) = -2j\int_{0}^{+\infty} x(t)\sin(2\pi ft) dt \\
\end{matrix}
$$

### Linearità

L'operazione di trasformazione secondo Fourier gode della **linearità**, quindi:
$$
\begin{rcases}
x(t) \leftrightarrow X(f) \\
y(t) \leftrightarrow Y(f)
\end{rcases}
\Rightarrow \alpha x(t) + \beta y(t) \leftrightarrow \alpha X(f) + \beta Y(f)\ \ \forall \alpha, \beta
$$

### Fattore di scala

Se il segnale originale viene **dilatato**, **compresso** o **invertito** anche la trasformata può essere direttamente calcolata dal segnale scalato:
$$x(t) \leftrightarrow X(f) \Rightarrow x(\alpha t) \leftrightarrow \frac{1}{\alpha} X\left(\frac{f}{\alpha}\right)$$

### Ritardo

Anche per il ritardo di un segnale la trasformata può essere calcolata immediatamente:
$$x(t) \leftrightarrow X(f) \Rightarrow x(t - T) \leftrightarrow X(f) e^{-2\pi fT}$$

### Dualità

Esiste una reciprocità dei [[Dominio|domini]] tempo/frequenza, dal quale prende forma il [[Teorema di dualità|teorema di dualità]]
$$x(t) \rightarrow X(f) \iff X(t) \rightarrow x(-f)$$

## Caratteristiche
### Derivata

È possibile ottenere la trasformata della [[Derivate|derivata]] di una funzione $x(t)$ conoscendone la trasformata $X(f)$ moltiplicandola per un fattore $j2\pi f$, detto **fasore**
$$y(t) = \frac{d}{dt}x(t) = \int_{-\infty}^{+\infty} Y(f) e^{j2\pi ft} df \Rightarrow Y(f) = j2\pi f \cdot X(f)$$

### Integrale

È possibile ottenere la trasformata di un [[Integrale|integrale]] di una funzione $x(t)$ conoscendone la trasformata $X(f)$ nel seguente modo:
$$x(t) \leftrightarrow X(f) \Rightarrow \int_{-\infty}^{t} x(\xi) d\xi \leftrightarrow \frac{X(f)}{j2\pi f} + \frac{X(0)}{2} \delta(f)$$

### Convoluzione
La [[Convoluzione|convoluzione]] di due segnali nel dominio temporale è equivalente al prodotto dei segnali stessi nel dominio di frequenza
$$x(t) \leftrightarrow X(f); y(t) \leftrightarrow Y(f) \Rightarrow x(t) * y(t) \leftrightarrow X(f) \cdot Y(f)$$

### Prodotto
Similmente per la convoluzione si può intuire che, per il prodotto di due segnali, nel dominio delle frequenze si ha una convoluzione
$$x_{1}(t) \cdot x_{2}(t) \leftrightarrow X_{1}(f) * X_{2}(f)$$