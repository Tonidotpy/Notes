---
 Created: 2022-05-10 10:08
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Indipendenza lineare
Due [[Variabili aleatorie|variabili aleatorie]] sono **indipendenti linearmente** se $Cov(X, Y) = 0$

*Teorema*: L'[[Indipendenza stocastica|indipendenza stocastica]] => [[Indipendenza in media|indipendenza in media]] => **indipendenza lineare**.

###### Indice di correlazione (di Pearson)
$$-1 \le \delta(x, y) = \frac{Cov(X, Y)}{\sqrt{Var(X) \cdot Var(Y)}} \le 1$$
per **Cauchy-Schwartz**.
- Quando $\delta(X, Y) = 0$ allroa $X$ e $Y$ sono **linearmente indipendenti**;
- quando $|\delta(X, Y)| = 1$ allora $X$ e $Y$ sono **esattamente linearmente indipendenti**, cioè esistono $a$ e $b$ tali che $P(Y = ax + b) = 1$
In particolare quando questo accade allora i [[Valore atteso|valori attesi]] condizionati della $Y$ dato $X$ stanno sulla retta $ax + b$
- $R^{2} \equiv \delta^{2}$