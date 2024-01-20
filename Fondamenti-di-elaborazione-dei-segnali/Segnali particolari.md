---
Created: 2023-09-27 13:51
Author: Antonio Gelain
aliases: 
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Esistono dei particolari [[Segnale|segnali]] che vengono utilizzate o compaiono spesso nel campo dell'**elaborazione dei segnali**

---

## Funzione rettangolo simmetrico

$$A\Pi\left(\frac{t}{T}\right) = \begin{cases}
A & |t| \le \frac{T}{2} \\
0 & \text{altrove}
\end{cases}
$$
![funzione-rettangolo-simmetrico](https://didatticacuciuffo.altervista.org/wp-content/uploads/2023/01/rect-3.svg)

## Funzione gradino unitario

$$u(t) = \begin{cases}
1 & t \ge 0 \\
0 & \text{altrove}
\end{cases}$$
![funzione-gradino-unitario](https://didatticacuciuffo.altervista.org/wp-content/uploads/2023/01/gradino-Heaveside-2.svg)

## Funzione segno

$$s(t) = \begin{cases}
1 & t > 0 \\
-1 & t < 0
\end{cases}$$
>[!INFO] $u(t) = \frac{1}{2}(s(t) + 1)$

![funzione-segno](https://www.andreaminini.org/data/andreamininiorg/funzione-segno-grafico.gif)

## Funzione triangolo simmetrico

$$A\Sigma\left(\frac{t}{T}\right) \begin{cases}
A\frac{\frac{T}{2} - |t|}{\frac{T}{2}} & t \le \frac{T}{2} \\
0 & \text{altrove}
\end{cases}$$
![funzione-triangolo](https://www.electroyou.it/fidocad/cache/d9b425ff1a3eb873bde97cfcabfe3e3359a591d3_3_650.png)

## Funzione sinc

$$sinc(x) = \frac{\sin \pi x}{\pi x}$$
![funzione-sinc](https://www.electroyou.it/image.php?id=8077)
