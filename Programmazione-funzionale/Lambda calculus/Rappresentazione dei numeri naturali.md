---
 Created: 2022-06-18 19:29
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Rappresentazione dei numeri naturali
Nel [[Lambda calculus|lambda calculus]] il numero 0 viene codificato come $\lambda f.\lambda x.x$.
Secondo l'**assioma di Peano** se $n$ è un **numero naturale** lo stesso sarà anche il suo **successore**, ciò viene espresso applicando $f$ per $n$ volte:

| Numero | Rappresentazione                   |
| ------ | ---------------------------------- |
| 0      | $\lambda f.\lambda x.x$            |
| 1      | $\lambda f.\lambda x.f x$          |
| 2      | $\lambda f.\lambda x.f (f x)$      |
| 3      | $\lambda f.\lambda x.f (f (f x) )$ |
| ...    | ...                                |
| $n$    | $\lambda f.\lambda x.nf x$         |

Da cui si può ricavare la **funzione successore**:
$$succ(n) = \lambda n.\lambda f.\lambda x.f(nfx)$$