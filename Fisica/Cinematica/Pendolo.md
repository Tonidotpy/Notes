---
 Created: 2023-03-15 10:58
 Author: Antonio Gelain
 Aliases: []
 Tags: [cinematica]
---

Un **pendolo semplice** è un [[Sistema di riferimento|sistema]] fisico costituito da un filo **insetensibile** e da una [[Massa|massa]] puntiforme fissata alla sua estremità soggetta all'[[Gravità|attrazione gravitazionale]]

---

![Pendolo semplice](https://upload.wikimedia.org/wikipedia/it/thumb/5/58/Pendolo_semplice.jpg/220px-Pendolo_semplice.jpg)

Sia $l$ la [[Lunghezza|lunghezza]] del filo:
$$\begin{cases}
x = l \sin \cdot \theta \\
y = l - l \cdot \cos \theta
\end{cases}$$
$$\begin{cases}
v_{x} = \frac{dx}{dt} = l \cdot \cos \theta \cdot \frac{d\theta}{dt} \\
v_{y} = \frac{dy}{dt} = l \cdot \sin \theta \cdot \frac{d\theta}{dt}
\end{cases}$$
$$\begin{cases}
l[ -\sin \theta (\frac{d\theta}{dt})^{2} + \cos \theta \cdot \frac{d^{2}\theta}{dt^{2}} ]=-g\sin \theta \cos \theta \\
l[ \cos \theta (\frac{d\theta}{dt})^{2} + \sin \theta \cdot \frac{d^{2}\theta}{dt^{2}} ]=-g \sin^{2}\theta
\end{cases}
$$

## Equazione del moto armonico

Sia $\omega^{2} = \frac{g}{l}$ la [[Pulsazione|pulsazione]]:
$$\frac{d^{2}\theta}{dt^{2}} + \omega^{2}\theta = 0$$

$$\theta(t) = \theta_{0} \sin(\omega t + \phi)$$