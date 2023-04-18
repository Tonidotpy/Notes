---
 Created: 2022-12-25 17:21
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Classless Addressing, Indirizzamento Classless, CIDR]
 Tags: []
---

**Classless Inter-Domain Routing** (*CIDR*) è un metodo di **assegnazione** degli [[Indirizzo IPv4|indirizzi IP]] che viene utilizzato per **gestire** in modo più efficiente gli indirizzi IP e per risolvere alcuni problemi legati all'[[Indirizzamento Classful|indirizzamento classful]]

---

La suddivisione tra prefisso e suffisso è **completamente arbitraria**, vengono così eliminate le classi ottimizzando l'utilizzo di IP in base al numero di host presenti
Per conoscere la grandezza del prefisso (e del suffisso) non più fissata si utilizza una [[Subnet Mask|maschera di rete]]

La **notazione** del CIDR è come quella dell'indirizzo IP seguito da uno slash e un numero che rappresenta il numero di bit a `1` della subnet mask associata a quell'IP, ad esempio `192.168.1.25/24`

Per capire a che rete appartiene un indirizzo IP basta fare l'*AND bit-a-bit* con la maschera di rete associata e nel caso ci siano **corrispondenze multiple** si utilizza il **prefisso più lungo** (*longest prefix matching*)

Un vantaggio di questo tipo di indirizzamento è la possibilità di **aggregare** indirizzi IP cambiando la maschera di rete
Se una rete ha diverse sottoreti con IP diversi (es. `200.23.16.0/23`, `200.23.18.0/23`, ..., `200.23.30.0/23`) per ricevere tutti i messaggi indirizzati a quelle sottoreti si può utilizzare un **unico IP** (`200.23.16.0/20`) che li raggruppa invece di utilizzarli tutti singolarmente