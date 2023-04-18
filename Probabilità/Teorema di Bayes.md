---
 Created: 2022-03-30 14:08
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Teorema di Bayes
Consideriamo uno [[Spazio probabilizzato|spazio probabilizzato]] ($\Omega, \mathcal{A}, P$) e prendiamo una successione di eventi $\{ A_i \}_{i=1}^{+\infty}$ in modo che siano una [[Partizione|partizione]] di $\Omega$.
Assumiamo $P(A_{i}) > 0 \forall i$ allora dato un evento $B$ abbiamo che:

> $$P(A_{i}|B) = \frac{P(B|A_{i}) P(A_{i})}{\sum\limits_{j=1}^{\infty} P(B|A_{j})P(A_{j})}$$

---

##### Formule di Bayes
- $P(A|B) = \frac{P(B|A) P(A)}{P(B)}$[^1]
- $P(B|A) = \frac{P(A|B) P(B)}{P(A)}$

[^1]: Il denominatore delle formule di Bayes è ricavato dal **teorema di Bayes** che non è altro che il [[Teorema delle probabilità totali|teorema delle probabilità totali]].