---
 Created: 2024-01-22 12:00
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **quantizzazione uniforme** è un particolare tipo di [[Quantizzazione|quantizzazione]] in cui gli $M$ livelli sono **equispaziati**

---

L'errore massimo $\epsilon_{q}$ che posso commettere su un campione è pari in modulo a $\frac{\Delta}{2}$, con $\Delta$ costante
Dato in ingresso un [[Segnale|segnale]] normalizzato tra $\pm 1$ abbiamo che:
$$\Delta = \frac{2}{M} \Rightarrow |e_{q}^{max}| = \frac{\Delta}{2} = \frac{1}{M}$$

La quantizzazione introduce un errore sistematico, detto [[Rumore di quantizzazione|rumore di quantizzazione]], il cui valore è compreso tra $- \frac{\Delta}{2}$ e $\frac{\Delta}{2}$

Dal momento che la [[Potenza media di un segnale|potenza media del rumore]] coincide col [[Valore quadratico medio di un segnale|valore quadratico medio]], che a sua volta coincide con la [[Varianza di un segnale|varianza]], allora:
$$E\{ \epsilon_{q}^{2} \} = \sigma_{q}^{2} = \frac{\Delta^{2}}{12}$$

Il [[Rapporto segnale-rumore|rapporto segnale-rumore]] di un quantizzatore uniforme, dato un segnale a valor medio nullo e che varia uniformemnte in $[-\frac{A}{2}, \frac{A}{2}]$, è pari a:
$$SNR = 10 \log_{10} \frac{A^{2}}{\Delta^{2}} = 10 \log_{10} \frac{A^{2}}{\frac{A^{2}}{2^{2B}}} = 10 \frac{\log_{2} 2^{2B}}{\log_{2} 10} \simeq 6B$$
dove:
- $M$ è il numero di livelli di quantizzazione
- $B = \log_{2} M$ è il numero di [[Bit|bit]] del quantizzatore
