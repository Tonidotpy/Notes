---
 Created: 2023-10-04 15:23
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **serie di Fourier** è una rappresentazione di una [[Segnale periodico|funzione periodica]] mediante una combinazione lineare di funzioni sinusoidali

---

Un generico segnale periodico di periodo $T_{0}$ può essere sviluppato mediante la seguente serie:
$$x(t) = a_{0} + \sum\limits_{k = 1}^{\infty} a_{k} \cos{\left(\frac{2 \pi kt}{T_{0}} + \theta_{k} \right)}$$
Le oscillazioni della serie hanno frequenza multipla di $\frac{1}{T_{0}}$, detta **frequenza fondamentale**
Il termine $k$-esimo della serie è detto **armonica i ordine** $k$
Il termine $a_{0}$ (a frequenza nulla) è detto **componente continua**

A questo punto si può riscrivere la precedente formula in maniera più compatta come:
$$x(t) = \sum\limits_{n = -\infty}^{+\infty} X_{n} e^{j 2\pi n f_{0} t}$$
dove:
$$X_{n} = \begin{cases}
\frac{a_{n}}{2} e^{j \theta_{n}} & n > 0 \\
\frac{a_{-n}}{2} e^{j \theta_{-n}} & n < 0 \\
a_{0} & n = 0
\end{cases}$$

Si può dimostrare che il coefficiente $n$-esimo della serie è dato dal seguente integrale
$$X_{n} = \frac{1}{T_{0}} \int_{-\frac{T_{0}}{2}}^{\frac{T_{0}}{2}} x(t)e^{-j 2\pi n f_{0} t} dt$$

---

## Proprietà della serie

### Simmetria Hermitiana

I coefficienti $X_{n}$ godono della [[Simmetria Hermitiana|simmetria Hermitiana]], per cui:
$$X_{n} = -X_{-n}^{*} \iff \begin{cases}
|X_{n}| = |X_{-n}| \\
\arg{(X_{n})} = -\arg{(X_{-n})}
\end{cases}$$
### Linearità

Dati due [[Segnale periodico|segnali periodici]] $x(t)$ e $y(t)$, la rappresentazione della serie di Fourier è anche un'operazione **lineare**
$$z(t) = \alpha x(t) + \beta y(t) \Rightarrow Z_{k} = \alpha X_{k} + \beta Y_{k}$$

### Simmetria del segnale $x(t)$

Dato un segnale periodico **pari** $x(t)$, si dimostra che i coefficienti $X_{n}$ saranno **reali**, per cui la serie sarà costituita da soli **coseni**
$$X_{k} = \frac{2}{T_{0}} \int_{0}^{\frac{T_{0}}{2}} x(t) \cos{(2 \pi k f_{0} t)} dt$$

Dato un segnale periodico **dispari** $x(t)$, si dimostra che i coefficienti $X_{n}$ saranno **immaginari**, per cui la serie sarà costituita solo da **seni**
$$X_{k} = -\frac{2}{T_{0}} \int_{0}^{\frac{T_{0}}{2}} x(t) \sin{(2 \pi k f_{0} t)} dt$$

### Segnali alternati

Definiamo **segnali alternati** come dei segnali periodici la cui semionda negativa ha andamento speculare a quella positiva, di conseguenza i segnali hanno sempre [[Valore medio di un segnale|valor medio]] **nullo**
Si dimostra perciò che nei segnali alternati i coefficienti corrispondenti alle armoniche pari sono **nulli**