---
 Created: 2022-05-12 08:47
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Grado di un vertice
SIa $G = (V, E)$ un [[Grafi finiti|grafo finito]] e sia $v \in V$.
Si dice **grado di $v$ in $G$** il seguente numero naturale:
$$deg_{G}(V) := ||\{ e \in E\ |\ v \in e \}$$
ossia il numero di lati connessi al vertice $v$.

Sia $G = (V, E)$ un [[Grafi finiti|grafo finito]], vale:
$$\sum\limits_{v \in V} deg_{G}(V) = 2|E|$$
