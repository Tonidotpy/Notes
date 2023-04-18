---
 Created: 2022-05-18 14:18
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Intervallo di confidenza, Regione di confidenza]
 Tags: []
---

# Stima intervallare
Sia $X \sim N(\mu, \sigma^{2})$ con $\sigma^{2}$ **noto**.
Lo [[Stimatore|stimatore]] è $\hat{\mu} = \overline{X_{n}} \sim N(\mu, \frac{\sigma^{2}_{o}}{n})$.
$$Z_{n} = \sqrt{n} \frac{\overline{X_{n}} - \mu}{\sigma_{n}} \sim N(0, 1)$$
$$P(x_{\frac{a}{2}} \le Z_{n} \le z_{1 - \frac{a}{2}}) = 1 - a$$