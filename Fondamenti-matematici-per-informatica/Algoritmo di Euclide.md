---
Created: 2022-03-29 16:57
Author: Antonio Gelain
aliases: 
tags:
---

# Algoritmo di Euclide

Dati $n, m \in \mathbb{Z} \backslash \{ 0 \}$ con $m \ne 0$.
Eseguiamo la divisione di $n$ per $m$ ottenendo un quoziente $q$ con resto $r$:
$$\begin{cases} n = qm + r\\ 0 \le r < |m| \end{cases}$$
Vale:
$$\{ c \in \mathbb{Z}\ |\ \frac{n}{c}, \frac{m}{c} \} = \{ c \in \mathbb{Z}\ |\ \frac{m}{c}, \frac{r}{c} \}$$
In particolare $MCD(n, m) = \max(A) = \max(B) = MCD(m, r)$

- L'algoritmo non dipende dal *segno* dei valori ne dalla loro *posizione*.

Supponendo $0 \le m < n$:
1. Se $m = 0$;
	1. l'$MCD$ è $n$;
2. altrimenti;
	1. si calcola il resto $r$ della divisione tra $n$ ed $m$;
	2. si pone $n = m$;
	3. si pone $m = r$;
	4. si ripete il procedimento dall'inizio.