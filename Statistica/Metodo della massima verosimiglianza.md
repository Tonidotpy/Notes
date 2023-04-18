---
 Created: 2022-05-25 14:12
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Metodo della massima verosimiglianza
$$X_{i} \sim N(\mu, \sigma^{2})$$
$$f_{X_{1}, ..., X_{n}} (x_{1}, ..., x_{n})
	= f_{X_{1}}(x_{1}) \cdot ... \cdot f_{X_{n}}(x_{n})
	= \prod_{i=1}^{n} f_{X_{i}}(x_{i})
	= (2 \pi \sigma^{2})^{-\frac{n}{2}} \exp(- \frac{1}{2\sigma^{2}} \sum\limits_{i?1}^{n} (x_{i} - \mu)^{2})$$
### Log-verosimiglianza
$$-\frac{n}{2} \log(2 \pi \sigma^{2}) \exp(- \frac{1}{2\sigma^{2}} \sum\limits_{i?1}^{n} (x_{i} - \mu)^{2})$$