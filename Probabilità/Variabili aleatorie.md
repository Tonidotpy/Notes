---
 Created: 2022-04-12 10:12
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Variabili casuali, Variabili statistiche]
 Tags: []
---

# Variabili aleatorie
*Def*: La funzione $x(\omega)$ è detta **variabile aleatoria** se per ogni $A \in B(\mathbb{R})$ la sua antiimmagine $A^{-1} \in A$ è un evento


## Variabili aleatorie doppie
### Variabili aleatorie doppie discrete
Sono caratterizzate da:
- Probabilità congiunta: $p_{X, Y}(x, y) = P(\{ X = x \} \cap \{ Y = y \})$;
- Funzione di distribuzione: $F_{X, Y}(x, y) = P(\{ X \le x \} \cap \{ Y \le y \})$;
- $P(\{ x_{1} < X \le x_{2} \} \cap \{ y_{1} < Y \le y_{2} \}) = F_{X, Y}(x_{2}, y_{2}) - F_{X,Y}(x_{1}, y_{2}) - F_{X, Y}(x_{2}, y_{1}) + F_{X, Y}(x_{1}, y_{1})$;
- $p_{X}(x) = P(\{ X = x \}) = \sum\limits_{y \in R_{Y}} p_{X, Y}(x, y)$ -> **probabilità marginale** della **variabile aleatoria** $X$;
- $F_{X}(x) = P(\{ X \le x \}) = \sum\limits_{u \le x} \sum\limits_{y \in R_{Y}} p_{X, Y}(x, y)$ -> funzione di **distribuzione marginale** della **variabile aleatoria** $X$.

In generale data una **variabile aleatoria bivariata discreta** $(X, Y) \sim P_{X, Y}(x, y)\ \ \ \ x \in R_{X}, y \in R_{Y}$ allora:
- per ogni $y \in R_{Y}$ avrò una **variabile aleatoria** $X|Y = y \sim P_{X|Y}(x|y)\ \ \ \ \forall x \in R_{X}$;
- per ogni $x \in R_{X}$ avrò una **variabile aleatoria** $Y|X = x \sim P_{Y|X}(y|x) \ \ \ \ \forall y \in R_{y}$.

### Variabili aleatorie bivariate continue
Sono caratterizzate da:
- funzione di **densità congiunta** $f_{X, Y}(x, y)$ tale che:
	1. $f_{X, Y}(x, y) \ge 0\ \ \ \ \forall(x, y) \in \mathbb{R}^2$;
	2. $\int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} f_{X, Y}(x, y)dy\ dx = 1$;
- funzione di **densità marginale** della **variabile aleatoria** $X$: $f_{X}(x) = \int_{-\infty}^{+\infty} f_{X, Y}(x, y) dy$;
- $F_{X}(x) = \int_{-\infty}^{x} \int_{-\infty}^{+\infty} f_{X, Y}(u, y) dy\ du$;
- $F_{X, Y}(x, y) = \int_{-\infty}^{x}\int_{-\infty}^{y} f_{X, Y}(u, v) dv\ du$;
- $P(\{ x_{1} < X \le x_{2} \} \cap \{ y_{1} < Y \le y_{2} \}) = \int_{x_{1}}^{x_{2}} \int_{y_{1}}^{y_{2}} f_{X, Y}(u, v) dv\ du$;
- $F_{X}(x) = \lim_{y \to +\infty} F_{X, Y}(x, y)$.

### Probabilità condizionata delle variabili aleatorie bivariate
Dato uno [[Spazio probabilizzato|spazio probabilizzato]] $(\Omega, A, \mathcal{P})$ e due [[Esito|eventi]] $A$ e $B$ con $\mathcal{P} > 0$ allora $P(A | B) = \frac{P(A \cap B)}{P(B)}$
Supponiamo che $(X, Y)$ sia una **variabile aleatoria bivariata discreta** $A = \{ \omega \in \Omega\ |\ X(\omega) = x \} = \{ X = x \}$    $B = \{ \omega \in \Omega\ |\ Y(\omega) = y \} = \{ Y = y \}$

La [[Probabilità condizionata|probabilità condizionata]] della **variabile aleatoria** $X$ rispetto alla **variabile aleatoria** $Y$ è:
$$P_{X|Y}(x|y) = P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(\{X = x\} \cap \{ Y = y \})}{P(\{ Y = y \})} = \frac{P_{X, Y}(x, y)}{P_{r}(y)}$$
$$p_{X, Y}(x, y) = p_{r}(y) p_{X|Y}(x|y) = p_{X}(x)p_{Y|X}(y|x)$$