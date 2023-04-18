---
 Created: 2022-03-29 16:49
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Numeri coprimi
Dati $n, m \in \mathbb{Z} \backslash \{ 0 \}$ diciamo che $n$ e $m$ sono **coprimi**, oppure *primi tra loro* se $MCD(n, m) = 1$

---

Osserviamo che se $\frac{n}{MCD(n, m)}, \frac{m}{MCD(n, m)}  \Rightarrow  \frac{xn + ym = 1}{MCD(n, m) > 0}$

- Se $d := MCD(n, m)$ allora $\frac{n}{d}, \frac{m}{d} \in \mathbb{Z}$ ossia $MCD\left(\frac{n}{d}, \frac{m}{d}\right)= 1$

Siano $n, m \in \mathbb{Z}$ non entrambi nulli o sia $q \in \mathbb{Z}$.
Supponiamo $MCD(n, m) = 1$
Valgono le seguenti proposizioni:
1. $\frac{mq}{n} \Rightarrow \frac{q}{n}$;
2. $\frac{q}{n}$ e $\frac{q}{m} \Rightarrow \frac{q}{nm}$;