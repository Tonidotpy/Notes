---
 Created: 2021-10-12 16:03
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [matematica,analisi,limiti]
---

# Limiti notevoli

###### Definizione

I **limiti notevoli** sono particolari limiti di [[Funzioni elementari|funzioni elementari]] aventi [[Forme indeterminate|forme indeterminate]] ricorrenti che vengono dimostrati una volta per tutte e dati per buoni nel calcolo dei **limiti**.

---

| N°  | Limite                                                  | Forma indeterminata   |
|:--- |:------------------------------------------------------- |:--------------------- |
| 1   | $$\lim_{x \to 0} \frac{\sin{x}}{x} = 1$$                | $$\frac{0}{0}$$       |
| 2   | $$\lim_{x \to \pm\infty} (1 + \frac{1}{x})^x = e$$        | $$1^\infty$$          |
| 3   | $$\lim_{x \to 0}\frac{1 - \cos{x}}{x^2} = \frac{1}{2}$$ | $$\frac{0}{0}$$       |
| 4   | $$\lim_{x \to 0}\frac{e^x - 1}{x} = 1$$                 | $$\frac{0}{0}$$       |
| 5   | $$\lim_{x \to 0}\frac{\ln{(1 + x)}}{x} = 1$$            | $$\frac{0}{0}$$       |
| 6   | $$\lim_{x \to 0}\frac{\tan{x}}{x} = 1$$                 | $$\frac{0}{0}$$       |
| 7   | $$\lim_{x \to 0}\frac{\arctan{x}}{x} = 1$$              | $$\frac{0}{0}$$       |
| 8   | $$\lim_{x \to 0}\frac{\arcsin{x}}{x} = 1$$              | $$\frac{0}{0}$$       |
| 9   | $$\lim_{x \to 0}\frac{a^x - 1}{x} = \ln{a}$$            | $$\frac{0}{0}$$       |
| 10  | $$\lim_{x \to 0^+}x \ln{x} = 0$$                        | $$0 \cdot (-\infty)$$ |

---

###### Dimostrazione

3. 
$$
\lim_{x \to 0} \frac{1 - \cos{x}}{x^{2}} = \lim_{x \to 0} \frac{1 - \cos{x}}{x^{2}} \cdot \frac{1 + \cos{x}}{1 + \cos{x}} = \lim_{x \to 0} \frac{1 - \cos^2{x}}{x^{2}} \cdot \frac{1}{1 + cos{x}} = \frac{1}{2}
$$
4. 
$$
\lim_{x \to 0} \frac{e^x - 1}{x} = \lim_{y \to 0} (\frac{\ln{(y + 1)}}{y})^{-1} = 1\ \ \ \ con\ y = e^x - 1
$$
5. 
$$
\lim_{x \to 0} \frac{\ln{(1 + x)}}{x} = \lim_{x \to 0} \frac{1}{x} \cdot \ln{(1 + x)} = \lim_{x \to 0} \ln{(1 + x)}^\frac{1}{x} = 
\begin{cases}
	\lim_{y \to +\infty} \ln{(1 + \frac{1}{y})}^y = \ln{e} = 1\\
	\lim_{y \to -\infty} \ln{(1 + \frac{1}{y})}^y = \ln{e} = 1
\end{cases}
$$

###### Esempi