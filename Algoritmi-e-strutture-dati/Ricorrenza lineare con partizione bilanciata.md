---
 Created: 2023-01-06 20:30
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Una **ricorrenza lineare con partizione bilanciata** è un'[[Equazione di ricorrenza|equazione di ricorrenza]] che descrive come una **sequenza di numeri** cambia da un termine all'altro

---

Siano $a \ge 1$ e $b \ge 2$ *costanti intere* e $c > 0$ e $\beta \ge 0$ *costanti reali*
Data un'equazione di ricorrenza $$
T(n) = \begin{cases}
aT\left(\frac{n}{b}\right) + cn^{\beta}& n > 1 \\
d & n \le 1
\end{cases}
$$
Poniamo $\alpha = \log_{b}{a}$, allora possiamo dire che $$
T(n) = \begin{cases}
\Theta(n^{\alpha}) & \alpha > \beta \\
\Theta(n^{\alpha} \log n) & \alpha = \beta \\
\Theta(n^{\beta}) & \alpha < \beta
\end{cases}
$$

---

Esiste un'**estensione** di questo tipo di ricorrenza
Siano $a \ge 1$, $b > 1$ e $f(n)$ *asintoticamente positiva*
Data un 'equazione di ricorrenza $$
T(n) = \begin{cases}
aT\left(\frac{n}{b}\right) + f(n) & n > 1 \\
d & n \le 1
\end{cases}
$$
Sono dati 3 casi:
1. $\exists \epsilon > 0\ |\ f(n) = O(n^{\log_{b} a - \epsilon}) \Rightarrow T(n) = \Theta(n^{\log_{b} a})$
2. $f(n) = \Theta(n^{\log_{b} a}) \Rightarrow T(n) = \Theta(f(n) \log n)$
3. $\exists \epsilon > 0\ |\ f(n) = \Omega(n^{\log_{b} a + \epsilon}) \land \exists c\ |\ 0 < c < 1,\exists m \ge 0\ |\ af\left(\frac{n}{b}\right) \le cf(n), \forall n \ge m \Rightarrow T(n) = \Theta(f(n))$

>[!INFO] I teoremi sopra citati non considerano equazioni di ricorrenza con interi **superiori** e/o **inferiori** ma valgono in ogni caso