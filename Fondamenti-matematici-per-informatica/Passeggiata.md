---
 Created: 2022-05-10 15:41
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Passeggiata
SIa $G = (V, E)$ un [[Grafi|grafo]].
Una [[Successioni|successione]] finita $(v_{0}, ..., v_{n})$ di vertici di $G$ si dice **passeggiata** in $G$ per $i \in \{ 1, ..., n \}$ (se $n \ge 1$), $\{ v_{i-1}, v_{i} \} \in E$ oppure $n = 0$.

### Proprietà
- Se $P = (v_{0}, ..., v_{n})$ è una **passeggiata** in $G$ allora $n$ si dice **lunghezza della passeggiata $P$** => $n = l(P)$;
- SIano $v$ e $w$ due vertici.
  DIciamo che $v$ è **congiungibile per passeggiate** (per [[Cammino|cammini]]) se esiste una **passeggiata** in $G$ della forma $(v = v_{0}, ..., v_{n} = w)$;
- SIa $G = (V, E)$ un [[Grafi|grafo]] e siano $v, w \in V$;
  Allora $v$ è **congiungibile a $w$ per passeggiata** $\iff$ $v$ è **congiungibile a $w$ per cammino**.
- $v, w \in V(G) = V(G')$, $G' \text{ è connesso } \Rightarrow \exists P$ passeggiata in $G'$ da $v$ a $w$ in quanto $E(G') \subset E(G)$.