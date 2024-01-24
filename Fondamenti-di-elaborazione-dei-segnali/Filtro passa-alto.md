---
Created: 2023-12-09 18:03
Author: Antonio Gelain
aliases:
  - HPF
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

Un **filtro passa-alto** è un tipo di [[Filtro lineare tempo-invariante|filtro LTI]] la cui [[Frequenza di taglio|frequenza di taglio]] inferiore $f_{1}$ è un numero maggiore di 0, passano perciò tutte le frequenze superiori ad $f_{1}$

---

Un filtro passa-alto può essere realizzato dal corrispondente passa-basso sottraendolo al segnale originale

Nel dominio discreto vengono principalmente utilizzati come **kernel** per l'HPF:
- Il [[Filtro gradiente|filtro gradiente]]
- Il [[Filtro pseudo-Laplaciano|filtro pseudo-Laplaciano]]

>[!NOTE] La [[Addizione|somma]] dei coefficienti di un kernel LPF deve essere pari a 1s

