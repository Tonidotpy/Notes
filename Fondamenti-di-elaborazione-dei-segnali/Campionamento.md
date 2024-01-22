---
 Created: 2024-01-22 10:42
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Il **campionamento** è una tecnica che consiste nel convertire un [[Segnale|segnale]] **continuo** nel [[Tempo|tempo]] oppure nello [[Spazio|spazio]] in un segnale **discreto**, valutandone l'[[Ampiezza|ampiezza]] solitamente ad intervalli regolari
$$x[n] = x(n T_{c})$$
dove:
- $x[n]$ è il valore $n$-esimo chiamato anche **campione**
- $x(t)$ è il valore assunto dal segnale nell'istante $nT_{c}$

---

>[!WARNING] L'operazione di campionamento perde qualsiasi informazione sull'andamento del segnale tra due impulsi successivi

Questo tipo di operazione si può ottenere moltiplicando il segnale per un [[Treno di impulsi|treno di impulsi]]
$$x_{c}(t) = \sum\limits_{n = -\infty}^{\infty} x(nT_{c}) \delta(t - nT_{c})$$

## Spettro di un segnale campionato

Lo [[Spettro di un segnale|spettro]] di un segnale campionato è uno spettro **periodico** con periodicità pari alla [[Frequenza|frequenza di campionamento]] $f_{c} = \frac{1}{T_{c}}$ la cui ampiezza è pari a $f_{c}$

Per ricostruire il segnale continuo partendo da quello digitale è possibile applicare un [[Filtro passa-basso|filtro passa-basso]] allo spettro del segnale campionato; tuttavia se la frequenza di campionamento è tale da permettere la sovrapposizione delle repliche nello spettro si otterrà il fenomeno dell'[[Aliasing di un segnale|aliasing]]

![aliasing-segnale](https://www.researchgate.net/publication/265108421/figure/fig31/AS:669438839889921@1536618065292/Figura-45-Tipica-manifestazione-del-fenomeno-dellaliasing.png)
