---
 Created: 2022-05-25 14:10
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Metodo dei minimi quadrati
$$\mu = argmin(\sum\limits_{i=1}^{n} (x_{i} - \mu)^{2})$$
$$\frac{\delta}{\delta \mu} \sum\limits_{i=1}^{n} (x_{i} - \mu) = \sum\limits_{i=1}^{n} -2 \cdot (x_{i} - \mu) = 0$$
### Equazione di stima ai minimi quadrati
$$\sum\limits(x_{i}- \mu) = 0$$
$$\sum\limits x_{i} - n\mu = 0\ \ \ \ \mu = \frac{\sum\limits_{i=1}^{n} x_{i}}{n} = \overline{x_{n}}$$
