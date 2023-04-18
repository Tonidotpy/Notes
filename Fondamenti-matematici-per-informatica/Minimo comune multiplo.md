---
 Created: 2022-03-31 10:05
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Minimo comune multiplo
Siano $n, m \in \mathbb{Z}$ e siano $M \in \mathbb{Z}$ tale che $M \ge 0$.
Diciamo che $M$ è un **minimo comune multiplo**(*mcm*) tra $n$ e $m$ se valgono:
1. $\frac{M}{n}$ e $\frac{M}{m}$.

---

- Se $n = m = 0$ allora l'$mcm(n, m) = 0$;
- Se $n$ e $m$ non sono entrambi *nulli* allora $mcm(n, m) = \frac{n * m}{MCD(n, m)}$.