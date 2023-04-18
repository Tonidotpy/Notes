---
 Created: 2022-04-20 14:10
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Speranza matematica]
 Tags: []
---

# Valore atteso
Data una [[Variabili aleatorie|variabile aleatoria]] $X$ definiamo il suo **valore atteso** (*se esiste*) nel seguente modo:
$$|E(X) = \begin{cases} \sum\limits x p_{X}(x)\ \ \ \ se\ x\text{ è discreta con supporto } R_{x} \\
\int_{-\infty}^{+\infty} x f_{X}(x)dx\ \ \ \ se\ x\text{ è continua} \end{cases}$$
Il **valore atteso** è definito se:
$$\sum\limits_{x \in R_{x}} |x| p_{X}(x) < \infty \text{    se x è discreta}$$
$$\int |x| f_{X}(x) < \infty \text{    se x è continua}$$
### Proprietà
Consideriamo la [[Variabili aleatorie|variabile aleatoria]] $X$ e due costanti $a, b\ a \ne 0$ e la [[Variabili aleatorie|variabile aleatoria]] $Y = aX + b\ y = ax + b$
$$P(Y = y) = P\left(X = \frac{y-b}{a}\right)$$
Se $X$ è discreta, allora $Y$ è discreta:
$$|E(Y) = \sum\limits_{y \in R_{Y}} p_{r}(y) = \sum\limits_{x \in R_{x}} (ax + b) p_{X}(x) = a |E(X) + b$$