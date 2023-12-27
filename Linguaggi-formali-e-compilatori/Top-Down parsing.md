---
 Created: 2023-12-27 18:39
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

**Top-down parsing** è una tecnica utilizzata dai [[Analisi sintattica|parser]] e consiste nella costruzione di una [[Derivazione|derivazione]] **leftmost**, perciò si procede dalla radice verso le foglie dell'[[Albero di derivazione|albero di derivazione]]

---

Spesso non è così intuitivo capire cosa conviene espandere per verificare che una parola appartenga alla [[Grammatica generativa|grammatica]] e se si arriva ad un ramo dell'albero di derivazione che non porta ad alcun risultato si è costretti a tornare indietro e provare con un altro ramo, il che non è molto efficiente
