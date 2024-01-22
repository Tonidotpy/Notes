---
 Created: 2024-01-20 19:03
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **larghezza di banda** di un [[Segnale|segnale]] è definita come l'intervallo di [[Frequenza di un segnale|frequenze]] per le quali lo [[Spettro di un segnale|spettro]] del segnale assume valori **non nulli**

---

Si può approssimare la larghezza di banda di un segnale utilizzando il [[Teorema di Rayleigh|teorema di Rayleigh]]; per esempio, si può fissare la banda $B$ come la frequenza entro la quale è incluso il `99%` di [[Energia di un segnale|energia del segnale]]
$$B: \int_{-B}^{B} |X(f)|^{2} df = 0.99 Ex$$

## Sistemi LTI
La larghezza di banda (o *banda passante*) di un [[Sistema lineare tempo-invariante|sistema LTI]] viene definita come la **massima** frequenza per cui il sistema fa passare una quantità *non trascurabile* di energia del sistema

>[!NOTE] L'approssimazione comunemente adottata è la cosiddetta ==banda a 3dB==

Dato il [[Fattore di guadagno|guadagno]] di un sistema in funzione della frequenza $G(f) = |H(f)|^{2}$, si definisce banda passante del sistema come la frequenza oltre la quale il guadagno del sistema scende di 3 decibel rispetto al picco:
$$B = f_{max} : G_{dB}(f_{max}) \ge -3dB$$
