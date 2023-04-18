---
 Created: 2022-03-29 10:18
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Teorema delle probabilità totali
Assumendo che $\wp(A_{n}) > 0$ per tuti gli $A_{n}$ allora:
	$$P(B) = P(\bigcup_{n=1}^{\infty} (A_{n} \cap B)) = \sum\limits_{n=1}^{\infty} P(A_{n} \cap B) = \sum\limits_{n=1}^{\infty} P(B|A_{n}) \cdot P(A_{n})$$