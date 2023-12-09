---
Created: 2023-12-09 17:43
Author: Antonio Gelain
aliases:
  - Filtro LTI
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Un **filtro lineare tempo-invariante** (o *filtro LTI*) è un tipo di [[Sistema lineare tempo-invariante|sistema LTI]] che opera una qualche trasformazione su di un [[Segnale|segnale]]

---

Un filtro LTI può amplificare o attenuare le [[Frequenza di un segnale|frequenze]] già presenti ma non può generarne di nuove

Esistono diverse tipologie di filtri LTI:
- [[Filtro passa-tutto]]
- [[Filtro passa-basso]]
- [[Filtro passa-alto]]
- [[Filtro passa-banda]]
- [[Filtro elimina-banda]]

La [[Risposta in frequenza|risposta in frequenza]] di un segnale filtrato risulta essere:
$$H(f) = \begin{cases}
ke^{-j2\pi ftd} & f_{1} < f < f_{2} \\
0 & \text{altrove}
\end{cases}$$
Dove $f_{1}$ è la [[Frequenza di taglio|frequenza di taglio]] inferiore ed $f_{2}$ è la frequenza di taglio superiore