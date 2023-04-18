---
 Created: 2023-01-03 19:30
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Metodo dell'albero di ricorsione]
 Tags: []
---

L'**analisi per livelli** (o metodo dell'albero di ricorsione) è un metodo utilizzato per la risoluzione delle [[Equazione di ricorrenza|equazioni di ricorrenza]]

---

La ricorrenza viene "srotolata" in vari **livelli** di cui viene calcolato il costo

Ad esempio, data un equazione di ricorrenza:
$$T(n) = \begin{cases}
T\left(\frac{n}{2} + b\right) & n > 1 \\
c & n \le 1
\end{cases}$$
Assumiamo che $n = 2^k$ ossia $k = \log(n)$
È possibile risolverla nel modo seguente:
$$\begin{split}
T(n) & = b + T\left(\frac{n}{2}\right) \\
& = b + b + T\left(\frac{n}{4}\right) \\
& = ... \\
& = b\log(n) + T(1)
\end{split}$$
Pericò l'equazione si può **semplificare** nel modo seguente:
$$T(n) = b\log(n) + c = \Theta(\log(n))$$
