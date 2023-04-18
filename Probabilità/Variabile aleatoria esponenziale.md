---
 Created: 2022-05-03 10:09
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Variabile aleatoria esponenziale
Fissato $\lambda > 0$ $x \sim \exp(\lambda)$ se:
$$f_{X}(x) = \lambda \exp(-\lambda x)\mathbb{1}(x > 0) = \begin{cases} \lambda e^{-\lambda x}\ \ \ \ se\ x>0\\ 0\ \ \ \  altrimenti \end{cases}$$
$$\mathbb{1}(x>0) = \begin{cases} 1\ \ \ \ se\ x>0\\ 0\ \ \ \ altrimenti \end{cases}$$
$$F_{X}(x) = \begin{cases} \int_{0}^{x}f_{X}(t)dt = \int_{0}^{x}\lambda e^{-\lambda t}dt = 1 - e^{-\lambda t}\ \ \ \ se\ x>0 \\
0\ \ \ \ altrimenti\end{cases}$$
###### Proprietà di assenza di memoria
$$P(X > x+y\ |\ X > y) = P(X > x)$$

Se $Y(x)$ è una funzione strettamente monotona e derivabile in un intervallo $(a, b)$ allora la **variabile aleatoria** $Y$ è dotata di densità:
$$\alpha = \min(Y(a), Y(b))\ \ \ \ \beta = max(Y(a), Y(b))$$
$$f_{r}(y) = \begin{cases} f_{x}(Y^{-1}(y) |\frac{d}{dy} Y^{-1}(y)|)\\
0\ \ \ \ altrove \end{cases}$$
