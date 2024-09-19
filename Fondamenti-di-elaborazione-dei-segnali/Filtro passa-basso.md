---
Created: 2023-12-09 18:00
Author: Antonio Gelain
aliases:
  - LPF
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Un **filtro passa-basso** è un tipo di [[Filtro lineare tempo-invariante|filtro LTI]] la cui [[Frequenza di taglio|frequenza di taglio]] superiore $f_{2}$ è un numero maggiore di 0, passano perciò tutte le frequenze minori di $f_{2}$

---

La [[Risposta in frequenza|risposta in frequenza]] di un filtro passa-basso è la seguente:
$$H_{LPF}(f) = G \Pi\left(\frac{f}{2 B_{pass}}\right) e^{-j 2 \pi f t_{0}}$$
Dove $G$ è il [[Fattore di guadagno|guadagno]] del filtro

Il filtro passa-basso è quello più semplice da realizzare

Nel dominio discreto vengono principalmente utilizzati come **kernel** per l'LPF:
- La [[Media mobile|media mobile]]
- Il [[Filtro gaussiano|filtro gaussiano]]

>[!NOTE] La [[Addizione|somma]] dei coefficienti di un kernel LPF deve essere pari a 1s

