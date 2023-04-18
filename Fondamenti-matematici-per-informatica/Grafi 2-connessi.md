---
 Created: 2022-05-12 10:04
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Grafi 2-connessi
Sia $G$ un [[Grafi|grafo]] e sia $v \in V(G)$.
Supponiamo che $G$ possiede almeno due vertici.
Definiamo un grafo $G-v$ ponendo:
$$V(G-v) := V(G) \backslash \{ V \}$$
$$E(G-V) := \{ e \in E(G)\ |\ v \notin e \}$$
Un grafo $G$ si dice **2-connesso** se possiede almeno 3 vertici e, per ogni $v \in V(G)$, $G-v$ è connesso.