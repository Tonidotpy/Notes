---
 Created: 2023-01-03 19:42
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Analisi per sostituzione]
 Tags: []
---

L'**analisi per sostituzione** è un metodo utilizzato per risolvere le [[Equazione di ricorrenza|equazioni di ricorrenza]]

---

É un metodo in cui si tenta di "indovinare" una soluzione in base alla propria **esperienza** e si dimostra che questa soluzione è correttà per [[Principio di induzione|induzione]]

Ad esempio, data una equazione di ricorrenza:
$$T(n) = \begin{cases}
T\left(\lfloor \frac{n}{2} \rfloor\right) + n & n > 1 \\
1 & n \le 1
\end{cases}$$
**Dimostriamo** che $T(n) = \Theta(n)$ per induzione

#### Limite superiore

**Caso base**: $T(1) = 1 \le 1 \cdot c \iff \forall c \ge 1$
**Ipotesi induttiva**: $\forall k < n\ |\ T(k) \le ck$
**Passo induttivo**:
$$\begin{split}
T(n) & = T\left(\lfloor \frac{n}{2} \rfloor\right) + n \\
& \le c\lfloor \frac{n}{2} \rfloor + n \\
& \le \frac{cn}{2} + n \\
& = \left(\frac{c}{2} + 1\right) n \\
& \le cn \\
& \iff \frac{c}{2} + 1 \le c \iff c \ge 2
\end{split}$$

Abbiamo quindi provato che $T(n) = O(n)$

#### Limite inferiore

**Caso base**: $T(1) = 1 \ge 1 \iff \forall d \le 1$
**Ipotesi induttiva**: $\forall k < n\ | \ T(k) \le dk$
**Passo induttivo**: $$\begin{split}
T(n) & = T\left(\lfloor \frac{n}{2} \rfloor\right) + n \\
& \le d \lfloor \frac{n}{2} \rfloor + n \\
& \le \frac{dn}{2} - 1 + n \\
& = \left(\frac{d}{2} - \frac{1}{n} + 1\right) \le dn \\
& \iff \frac{d}{2} - \frac{1}{n} + 1 \ge d \iff d \le 2 - \frac{2}{n}
\end{split}$$
Abbiamo quindi provato che $T(n) = \Omega(n)$
Perciò $T(n) = O(n) \land T(n) = \Omega(n) \iff T(n) = \Theta(n)$