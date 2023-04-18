---
 Created: 2022-03-10 09:48
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Teorema di ricorsione
> Sia $X$ un insieme non vuoto, sia $h: \mathbb{N} \times X \mapsto X$ e sia $c \in X$ allora esiste ed è unica una funzione $f : \mathbb{N} \mapsto X$ tale che:
> 1. $f(0) = c$;
> 2. $f(succ(n)) = h(n, f(n))\ \forall n \in \mathbb{N}$.

---

###### Applicazioni
Sia $m \in \mathbb{N}$.
Definiamo la funzione "*somma sulla sinistra con $m$*" ovvero "$\mathbb{N} \mapsto \mathbb{N}\ \ \ \ n \mapsto m + n$".
