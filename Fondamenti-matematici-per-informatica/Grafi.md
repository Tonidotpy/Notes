---
 Created: 2022-05-03 16:47
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Grafi
SIa $V$ un [[Insiemi|insieme]].
Indichiamo con ${V}\choose{2}$ l'[[Insiemi|insieme]] i cui elementi sono tutti i possibili 2-[[Sottoinsiemi|sottoinsiemi]] di $V$ (cioè i [[Sottoinsiem|sottoinsiemi]] di $V$ formati da due elementi)
Se la [[Cardinalità|cardinalità]] di $V$ è maggiore o uguale a 2 allora: $|{{V}\choose{2}}| = {{|V| }\choose{2}}$

Un **grafo** $G$ è una coppia $(V, E)$ dove:
- $V$ è un [[Insieme vuoto|insieme non vuoto]];
- $E \subset {V \choose 2}$.
In questo caso $G = (V, E)$, $V$ è l'[[Insiemi|insieme]] dei **vertici** di $G$ ed $E$ è l'[[Insiemi|insieme]] dei **lati** di $G$.
Inoltre se $e = \{ v, w \} \in E$ allora $v$ e $w$ sono detti **estremi** di $e$ e congiungono $v$ e $w$.