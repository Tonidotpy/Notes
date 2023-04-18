---
 Created: 2022-04-21 09:57
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Elementi invertibili modulo $n$
Siano $n > 0$ e $a \in \mathbb{Z}$.
Diciamo che $a$ è **invertibile modulo $n$** se $\exists x \in \mathbb{Z}\ |\ ax \equiv 1\ (mod\ n)$.
Equivalentemente diciamo che $[a]_{n}$ è **invertibile in $\frac{\mathbb{Z}}{n\mathbb{Z}}$** se $\exists [x]_{n} \in \frac{\mathbb{Z}}{n\mathbb{Z}}$
$$[x]_{n}[a]_{n} = [a]_{n}[x]_{n} = [1]_{n}$$
In questo caso $x \in \mathbb{Z}$ è un **inverso di $a$ modulo $n$** e $[x]_{n}$ è una classe inversa di $[a]_{n}$ in $\frac{\mathbb{Z}}{n \mathbb{Z}}$

###### Lemma
Supponiamo che $a$ sia invertibile modulo $n$, ovvero $[a]_{n}$ sia invertibile in $\frac{\mathbb{Z}}{n \mathbb{Z}}$.
Allora $\exists ! [x]_{n}$ inversa di $[a]_{n}$ in $\frac{\mathbb{Z}}{n\mathbb{Z}}$.
Inoltre tale classe $[x]_{n}$, vista come sottoinsieme di $\mathbb{Z}$, è **uguale** all'insieme di tutti gli elementi di $\mathbb{Z}$ inversi di modulo $n$.
In questo caso $[x]_{n}$ si indica $[a]^{-1}_{n} = \{ x \in \mathbb{Z}\ |\ ax \equiv 1\ (mod\ n) \}$.

###### Proposizione
$a \in \mathbb{Z}$ è invertibile modulo $n \iff \gcd(a, n) = 1$.
Inoltre se $a$ è invertibile modulo $n$ allora applicando l'[[Algoritmo di Euclide|algoritmo di Euclide]] ad $a$ ed $n$ otteniamo $x, y \in \mathbb{Z}$.
$$xa + ym = 1\ \ \ \ [a]_{n}^{-1}=[x]_{n}$$
