---
 Created: 2024-01-24 10:41
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Il **filtro gaussiano** è un [[Filtro passa-basso|filtro]] la cui [[Risposta all'impulso|risposta impulsiva]] è una [[Funzione gaussiana|funzione gaussiana]]

---

>[!NOTE] Più elevato è il valore della [[Varianza di un segnale|varianza]] $\sigma$, più aumenterà lo spread della gaussiana producendo una media più estesa e uniforme

Nel dominio discreto i campioni avranno valori:
$$h[k] = \frac{1}{\lambda} e^{- \frac{k^{2}}{2 \sigma^{2}}} : k \in \left[- \frac{K}{2}, \frac{K}{2}\right]$$
dove il **fattore di normalizzazione** è pari:
$$\lambda = \sum\limits_{k} e^{- \frac{k^{2}}{2 \sigma^{2}}}$$
e $K$ è proporzionale alla [[Deviazione standard|deviazione standard]]
