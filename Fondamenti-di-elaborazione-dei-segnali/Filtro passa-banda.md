---
 Created: 2023-12-09 18:05
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Un **filtro passa-banda** è un tipo di [[Filtro lineare tempo-invariante|filtro LTI]] in cui vengono fatte passare solamente le frequenze comprese tra le [[Frequenza di taglio|frequenza di taglio]] $f_{1}$ e $f_{2}$

---

La [[Risposta in frequenza|risposta in frequenza]] di un filtro passa-alto è la seguente:
$$H_{BPF}(f) = G \left[\Pi\left(\frac{(f - f_{c})}{B_{pass}}\right) + \Pi\left(\frac{(f + f_{c})}{B_{pass}}\right)\right] e^{-j 2 \pi f t_{0}}$$
Dove $G$ è il [[Fattore di guadagno|guadagno]] del filtro

Un filtro passa-banda può essere realizzato dalla combinazione di un [[Filtro passa-alto|filtro passa-alto]] ed uno [[Filtro passa-basso|passa-basso]]