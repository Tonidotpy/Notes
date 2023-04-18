---
 Created: 2022-05-18 13:45
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Teorema centrale del limite
Sia ${Y_{i}}^{\infty}_{i=1}$ una [[Successione di variabili aleatorie|successione di variabili aleatorie]] e $\mu = E(Y_{i})$, $\sigma^{2} = Var(Y_{i})$.
$$\overline{Y}_{n} = \frac{1}{n} \sum\limits_{i=1}^{n} Y_{i}\ \ \ \ E(\overline{Y}_{n}) = \mu\ \ \ \ Var(\overline{Y}_{n}) = \frac{Var(\overline{Y}_{1})}{n} = \frac{\sigma^{2}}{n}$$
$$Z_{n} = \frac{\overline{Y}_{n} - \mu}{\sqrt{\frac{\sigma^{2}}{n}}} = \sqrt{n} \cdot \frac{\overline{Y}_{n} - \mu}{\sigma}$$
$$\overline{Y}_{n} \sim N(\mu, \frac{\sigma^{2}}{n})$$