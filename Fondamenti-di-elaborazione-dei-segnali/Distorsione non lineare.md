---
 Created: 2023-12-11 10:59
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Una **distorsione non lineare** è un processo per cui un [[Segnale|segnale]] passa attraverso un [[Sistema distorcente|sistema distorcente non lineare]] modificandolo

---

Lo spettro di un segnale non lineare distorto, oltre che deformarsi, si **allarga**, ovvero occupa più [[Frequenza di un segnale|frequenze]], questa caratteristica non può avvenire nei [[Sistema lineare tempo-invariante|sistemi lineari]]

---

Per misurare le distorsioni non lineari si può immettere nel sistema un semplice segnale sinusoidale $x(t) = \cos(2\pi f_{0}t)$ ottenendo:
$$
\begin{matrix}
y(t) \approx a_{1}\cos(2\pi f_{0}t) + a_{2}[\cos^{2}(2\pi f_{0}t)] + a_{3}[\cos^{3}(2\pi f_{0}t)] = \\
= a_{1}\cos(2\pi f_{0}t) + a_{2}\left[\frac{1 + \cos(4\pi f_{0}t)}{2}\right] + a_{3}[\frac{1 + cos(4\pi f_{0}t)}{2}]\cos(2\pi f_{0}t)
\end{matrix}
$$
Raccogliendo i fattori otteniamo
$$y(t) \approx K + \alpha \cdot \cos(2\pi f_{0}t) + \beta \cdot\cos(2\pi 2f_{0}t) + ...$$
A parte la componente continue, i termini che danno più fastidio sono quelli a **frequenze multiple**; risulta utile misurare il rapporto percentuale tra l'ampiezza della prima armonica e quella della fondamentale, ottenendo la cosiddetta **distorsione di seconda armonica**: $|\frac{\beta}{\alpha}| \cdot 100$

>[!INFO] Se la non-linearità è pesante, può essere utile considerare anche la **distorsione di terza armonica**

---

Se la distorsione non è accettabile si può utilizzare una tecnica chiamata **companding**: in pratica faccio passare il segnale in un ulteriore sistema non lineare che ha lo scopo di limitare la dinamica del segnale alla zona di comportamento lineare del sistema (**compression**)