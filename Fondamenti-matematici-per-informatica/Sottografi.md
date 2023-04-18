---
 Created: 2022-05-03 17:19
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Sottografi
Siano $G = (V, E)$ e $G' = (V', E')$ due [[Grafi|grafi]], $G'$ è detto **sottografo** di $G$ se:
- $V' \subset V$;
- $E' \subset E$.
$G' = (V', E')$ si dice **sottografo indotto** da $V'$ se:
- $E' = \{ e \in E\ |\ e = \{ v, w \}, v, w \in V' \}$
Se $G'$ è **sottografo indotto** da $V'$ allora si scrive $G' = G[V']$.
