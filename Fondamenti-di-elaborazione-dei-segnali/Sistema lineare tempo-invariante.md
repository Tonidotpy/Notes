---
Created: 2023-09-28 08:56
Author: Antonio Gelain
aliases:
  - Sistema LTI
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Un **sistema lineare tempo-invarianti** (o *sistema LTI*) è particolare [[Sistema di elaborazione di segnali|sistema]] che gode di due proprietà:
1. **Linearità**
2. **Tempo-invarianza**

---

## Linearità

La proprietà di linearità, comunemente associata al **principio di sovrapposizione degli effetti**, viene definita come segue:
$$\begin{rcases}
f(x_{1}(t)) = y_{1}(t) \\
f(x_{2}(t)) = y_{2}(t)
\end{rcases} \Rightarrow f(\alpha x_{1}(t) + \beta x_{2}(t)) = \alpha y_{1}(t) + \beta y_{2}(t)\ \ \forall x_{1}(t), x_{2}(t), \alpha, \beta$$

Nel dominio discreto otteniamo:
$$\begin{rcases}
f(x_{1}[n]) = y_{1}[n] \\
f(x_{2}[n] = y_{2}[n]
\end{rcases} \Rightarrow f(\alpha x_{1}[n] + \beta x_{2}[n]) = \alpha y_{1}[n] + \beta y_{2}[n]\ \ \forall x_{1}[n], x_{2}[n], \alpha, \beta$$

## Tempo-invarianza

Tempo-invarianza significa che un sistema non modifica la propria risposta al variare del tempo
$$f(x(t)) = y(t) \Rightarrow f(x(t - t_{0})) = y(t - t_{0})$$

Nel dominio discreto si ottiene:
$$f(x[n]) = y[n] \Rightarrow f(x[n - k]) = y[n - k]$$

---

## Combinazione di sistemi LTI

### Serie
La [[Risposta in frequenza|risposta in frequenza]] di due sistemi LTI connessi in serie è pari al [[Moltiplicazione|prodotto]] delle loro risposte in frequenza:
$$H_{tot}(f) = H_{1}(f)H_{2}(f)$$

### Parallelo
La risposta in frequenza di due sistemi LTI connessi in parallelo è pari alla [[Addizione|somma algebrica]] delle loro risposte in frequenza:
$$H_{tot}(f) = H_{1}(f) \pm H_{2}(f)$$

### Retroazione negativa
La risposta in frequenza di due sistemi LTI configurati in maniera tale da avere una [[Retroazione negativa|retroazione negativa]] è pari a:
$$H_{tot}(f) = \frac{Y(f)}{U(f)} = \frac{H_{1}(f)}{1 + H_{1}(f)H_{2}(f)}$$

---

Dato un sistema LTI è possibile calcolare la [[Risposta di un segnale|risposta ad un segnale]] di ingresso $x(t)$ qualsiasi a partire dalla conoscenza della risposta dell'[[Delta di Dirac|impulso unitario]] $\delta(t)$

Prendiamo un segnale $x(t)$ e lo approssimiamo tramite una serie di forme d'onda rettangolari di durata $\Delta T$ e area unitaria
$$x_{R}(t) = \sum\limits_{k} x(k \Delta T) \cdot R(t - k \Delta T) \cdot \Delta T \approx x(t)$$

Osserviamo la risposta $h_{R}(t)$ del sistema al segnale $R(t)$ e poiché il sistema è LTI otteniamo la seguente formula
$$y_{R}(t) = \sum\limits_{k} x(k \Delta T) \cdot h_{R}(t - k \Delta T) \cdot \Delta T \approx y(t)$$

Intuitivamente utilizzando un $\Delta t$ molto piccolo si migliora l'approssimazione, perciò possiamo usare un $\Delta t$ tendente a zero ottenendo il [[Delta di Dirac|delta di Dirac]]
$$\lim_{\Delta t \mapsto 0} R(t) = \delta(t)$$
L'uscita $h_{R}(t)$ tende quindi alla [[Risposta all'impulso|risposta all'impulso]] che chiameremo $h(t)$, mentre per quanto riguarda $x_{R}(t)$ da [[Addizione|sommatoria]] di rettangoli diventerà il [[Limiti|limite]] di un [[Integrale|integrale]] di una serie infinita di impulsi coincidente con $x(t)$
$$\lim_{\Delta t \mapsto 0} x_{R}(t) = \int_{-\infty}^{+\infty} x(\tau) \delta(t - \tau) d\tau = x(t)$$

Stessa cosa vale per la **risposta del sistema**, che di conseguenza diventa l'[[Integrale di convoluzione|integrale di convoluzione]]
$$\lim_{\Delta t \mapsto 0} y_{R}(t) = \int_{-\infty}^{+\infty} x(\tau) h(t - \tau) d\tau = y(t) = x(t) \cdot h(t)$$

---

La **[[Banda|banda]] passante** di un sistema LTI viene definita come la **massima** frequenza per cui il sistema fa passare una quantità *non trascurabile* di energia del sistema di energia del sistema
L'approssimazione comunemente adottata è quella della cosiddetta **banda a 3dB**
$$B = f_{max} : G_{dB}(f_{max}) \ge -3dB$$

