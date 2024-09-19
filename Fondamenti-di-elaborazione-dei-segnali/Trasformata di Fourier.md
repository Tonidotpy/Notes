---
Created: 2023-10-11 14:28
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **trasformata di Fourier** è un'operazione che associa a una [[Funzione|funzione]] i valori dei **coefficienti** di questi sviluppi lineari, dandone in questo modo una rappresentazione nel [[Spettro di un segnale periodico|dominio delle frequenze]]
$$W(f) = \int_{-\infty}^{+\infty} w(t) e^{-j2\pi ft} dt$$

---

La trasformata di Fourier inversa è data dalla formula seguente:
$$w(t) = \int_{-\infty}^{+\infty} W(f) e^{j2\pi ft} df$$

---

La trasformata di Fourier può essere anche utilizzata per [[Segnale periodico|segnali periodici]] ottenendo un [[Treno di impulsi|treno di impulsi]] con [[Frequenza di un segnale|frequenza]] $\frac{1}{T}$, la cui [[Ampiezza|ampiezza]] è [[Modulazione|modulata]] dallo [[Spettro di un segnale periodico|spettro di Fourier]] del segnale di base
$$X(f) = \sum\limits_{k=-\infty}^{+\infty} \frac{1}{T} W\left(\frac{k}{T}\right) \delta\left(f - \frac{k}{T}\right)$$
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

È possibile ottenere la trasformata della [[Derivate|derivata]] di prim'ordine di una funzione $x(t)$ conoscendone la trasformata $X(f)$ moltiplicandola per un fattore $j2\pi f$, detto **fasore**
$$y(t) = \frac{d}{dt}x(t) = \int_{-\infty}^{+\infty} Y(f) e^{j2\pi ft} df \Rightarrow Y(f) = j2\pi f \cdot X(f)$$

È possibile inoltre generalizzare la formulazione precedente per derivate di qualsiasi ordine:
$$y(t) = \frac{d^{n}}{dt^{n}}x(t) \rightarrow (2 \pi jf)^{n} X(f)$$
### Integrale

È possibile ottenere la trasformata di un [[Integrale|integrale]] di una funzione $x(t)$ conoscendone la trasformata $X(f)$ nel seguente modo:
$$x(t) \leftrightarrow X(f) \Rightarrow \int_{-\infty}^{t} x(\xi) d\xi \leftrightarrow \frac{X(f)}{2\pi jf} + \frac{X(0)}{2} \delta(f)$$

### Convoluzione
La [[Convoluzione|convoluzione]] di due segnali nel dominio temporale è equivalente al prodotto dei segnali stessi nel dominio di frequenza
$$x(t) \leftrightarrow X(f); y(t) \leftrightarrow Y(f) \Rightarrow x(t) * y(t) \leftrightarrow X(f) \cdot Y(f)$$

### Prodotto
Similmente per la convoluzione si può intuire che, per il prodotto di due segnali, nel dominio delle frequenze si ha una convoluzione
$$x_{1}(t) \cdot x_{2}(t) \leftrightarrow X_{1}(f) * X_{2}(f)$$

### Modulazione
Dalla proprietà del prodotto si può ricavare la proprietà della modulazione, in pratica, modulando una sinusoide di frequenza $f_{0}$ otteniamo due repliche traslate in $\pm f_{0}$ dello spettro del segnale modulante

## Trasformate notevoli

### Segnale ritardato

L'integrale di Fourier nel caso di un segnale ritardato è il seguente:
$$x(t - T) \rightarrow Y(f) = \int_{-\infty}^{+\infty} x(t - T)e^{-2\pi jft} dt = \int_{-\infty}^{+\infty} x(\xi) e^{-2\pi jf(\xi + T)} d \xi = e^{-2 \pi jfT} \int_{-\infty}^{+\infty} x(\xi) e^{-2 \pi jf \xi} d \xi = e^{-2 \pi jfT} X(f)$$

>[!NOTE] L'oggetto $e^{-2 \pi jfT}$ viene chiamato [[Fasore|fasore]]

### Rettangolo

L'integrale di Fourier nel caso di una funzione rettangolo è il seguente:
$$x(t) = V_{0}\Pi\left(\frac{t}{T}\right) \rightarrow X(f) = \int_{-\frac{T}{2}}^{\frac{T}{2}} V_{0} e^{-2\pi jft} dt = \frac{V_{0}}{2\pi jf}[e^{\pi jfT} - e^{-\pi jfT}] = V_{0}T \frac{\sin{(\pi fT)}}{\pi fT} = V_{0}T \text{sinc}(fT)$$

### Triangolo

La funzione triangolo è data dall'operazione di convoluzione di due rettangoli con durata ed ampiezza uguali, di conseguenza la trasformata della funzione triangolo equivale al prodotto delle trasformate dei due triangoli:
$$[x_{1}(t) * x_{2}(t)] = x(t) = A\left(1 - \frac{|t|}{T}\right) \Rightarrow X(f) = \left[{\sqrt{\frac{A}{T}}} T \text{sinc}(fT)\right]\left[\sqrt{\frac{A}{T}} T \text{sinc}(fT)\right] = AT \text{sinc}^{2}(fT)$$

### Costante

Si può ottenere la trasformata di una funzione costante prendendo la funzione rettangolare e portando $T$ a infinito:
$$x(t) = V_{0}\Pi\left(\frac{t}{T}\right) \rightarrow X(f) = V_{0}T\text{sinc}(fT) \Rightarrow \lim_{T \mapsto +\infty} V_{0} \Pi \left(\frac{t}{T}\right) \equiv V_{0} \rightarrow V_{0}\delta(f)$$

### Delta di Dirac

La trasformata di Fourier del [[Delta di Dirac|delta di Dirac]] può essere ricavata da quella della costante utilizzando il teorema di dualità, nel seguente modo:
$$1 \rightarrow \delta(f) \Rightarrow \delta(t) \rightarrow 1 \ \forall f$$

### Fasore

Anche la trasformata del fasore può essere ricavata utilizzando il teorema di dualità come segue:
$$\delta(t - t_{0}) \rightarrow 1 \cdot e^{-2 \pi jft_{0}} = e^{-2 \pi jft_{0}}$$

### Sinc

La trasformata della sinc è ricavabile tramite dualità dalla funzione rettangolo:
$$x(t) = V_{0} \Pi \left(\frac{t}{T}\right) \rightarrow X(f) = V_{0} T \text{sinc}(fT) \Rightarrow V_{0} \text{sinc}(tB) \rightarrow x(-f) = V_{0} \frac{1}{B} \Pi \left(\frac{-f}{B}\right) = \frac{V_{0}}{B} \Pi \left(\frac{f}{B}\right)$$
### Esponenziale

Un'altra trasformata comune è quella dell'esponenziale causale:
$$\mathfrak{F}\{ e^{-\alpha t} \cdot 1(t) \} = \int_{0}^{+\infty} e^{-\alpha t} \cdot e^{-j2\pi ft} dt = \int_{0}^{+\infty} e^{-(\alpha + j2\pi f)t} dt = - \frac{e^{-(\alpha + j2 \pi f)t} \big|_{0}^{+\infty}}{\alpha + j2\pi f} = \frac{1}{\alpha + j2\pi f}$$

### Segno

La trasformata della funzione segno è relativamente complicata da calcolare, ma risulta essere pari a:
$$y(t) = 1 - \frac{2}{1 + e^{-at}} \ \ \ \ a > 0$$
$$\text{sign}(t) \rightarrow \lim_{a \rightarrow +\infty} Y(f) = \frac{1}{j \pi f}$$
### Sinusoidi

Anche i segnali sinusoidali sono molto comuni e la loro trasformata è particolarmente semplice:
$$
\begin{matrix}
x(t) = \cos(2\pi f_{0}t) \leftrightarrow X(f) = \frac{1}{2}[\delta(f + f_{0}) + \delta(f - f_{0})] \\
x(t) = \sin(2\pi f_{0}t) \leftrightarrow X(f) = \frac{j}{2}[\delta(f + f_{0}) + \delta(f - f_{0})]
\end{matrix}
$$
