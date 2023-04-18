---
 Created: 2023-01-10 17:35
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Una **ricorrenza lineare di ordine costante** è una speciale tipologia di [[Equazione di ricorrenza|ricorrenza lineare]], in cui l'**ordine**, ovvero il numero di termini precedenti utilizzati per calcolare un nuovo termine, è **costante**

---

Siano $a_{1}, a_{2}, ..., a_{h}$ *costanti intere* non negative, con $h$ costante positiva, $c$ e $\beta$ *costanti reali* tali che $c > 0$ e $\beta \ge 0$
Data un'equazione di ricorrenza $$
T(n) = \begin{cases}
\sum\limits_{1\le i \le h} a_{i} T(n - i) + cn^{\beta} & n > m \\
\Theta(1) & n \le m \le h
\end{cases}
$$
Poniamo $a = \sum\limits_{1 \le i \le h} a_{i}$, allora possiamo dire che $$
T(n) = \begin{cases}
\Theta(n^{\beta + 1}) & a = 1 \\
\Theta(a^{n} n^{\beta}) & a \ge 2
\end{cases}
$$