---
 Created: 2024-01-23 11:56
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Un **segnale discreto** è un [[Segnale|segnale]] composto da una [[Successione|serie]] di valori discreti nel [[Tempo|tempo]]

---

## Proprietà

### Simmetria
I segnali discreti possono presentare sia simmetria pari che dispari
$$
\begin{matrix}
x[n] = x[-n]\ \forall n \\
x[n] = -x[-n]\ \forall n
\end{matrix}
$$

### Guadagno
Nel caso di guadagno positivo si ha un'amplificazione del segnale altrimenti si ha un'attenuazione
$$
\begin{matrix}
\alpha x[n] : \alpha > 1 \\
\alpha x[n] : \alpha < 1
\end{matrix}
$$

### Ritardo
$$x[n - k]$$

### Fattore di scala
Nel dominio digitale compressione ed espansione corrispondono a **ricampionamenti**:
- **Sottocampionamento** (*compressione*): in cui occorre decimare i campioni e può introdurre [[Aliasing di un segnale|aliasing]]
- **Sovracampionamento** (*espansione*): occorre introdurre nuovi campioni nella sequenza per interpolazione o replica

### Integrazione
L'integrazione nel dominio discreto diventa una [[Addizione|somma]] cumulativa
$$y[n] = \sum\limits_{k=-\infty}^{n}x[k]$$

### Derivazione
La derivazione nel dominio discreto diventa una differenza finita
$$y[n] = \frac{1}{T_{c}}(x[n] - x[n - 1])$$
Data una sequenza $T_{c}$ potrebbe non essere noto, in questo caso si calcola solo la differenza tra i campioni

### Valor medio
Il valor medio nel dominio discreto viene calcolato utilizzando una somma:
$$\overline{x} = \lim_{K \rightarrow +\infty} \frac{1}{K} \sum\limits_{-\frac{K}{2}}^{\frac{K}{2}} x(k)$$

### Varianza
$$\sigma_{x} = \lim_{K \rightarrow +\infty} \frac{1}{K} \sum\limits_{-\frac{K}{2}}^{\frac{K}{2}} [ x(k) - \overline{x} ]^{2}$$
