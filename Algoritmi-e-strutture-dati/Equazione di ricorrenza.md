---
 Created: 2023-01-03 19:22
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Una **equazione di ricorrenza** è un'equazione che definisce una **sequenza** di numeri in **funzione** di numeri precedenti nella sequenza

---

Quando si calcola la [[Complessità di un algoritmo|complessità di un algoritmo]] ricorsivo, questa viene espressa tramite un'equazione di ricorrenza

Un'esempio di un equazione di ricorrenza per il [[Merge Sort]] è la seguente:
$$T(n) = \begin{cases}
T\left(\lfloor \frac{n}{2} \rfloor\right) + T\left(\lceil \frac{n}{2} \rceil\right) + \Theta(n) & n > 1 \\
\Theta(1) & n \le 1
\end{cases}$$

Esistono diversi metodi per **risolvere** le equazioni di ricorrenza:
- [[Analisi per livelli]]
- [[Analisi per tentativi]]
- [[Metodo dell'esperto]]