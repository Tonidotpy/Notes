---
 Created: 2022-06-18 20:05
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Rappresentazione della somma
La **somma** tra due **interi** $n, m$ viene tradotta in: "applica $f\ n$ volte al risultato dato dall'applicazione di $f\ m$ volte ad $x$", ossia:
$$\lambda n.\lambda m. \lambda f.\lambda x.nf(mfx)$$