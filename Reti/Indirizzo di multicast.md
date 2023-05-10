---
 Created: 2022-12-26 16:43
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Multicast]
 Tags: []
---

Un **indirizzo di multicast** è un [[Indirizzo IPv4|indirizzo IP]] che viene utilizzato per **inviare** un pacchetto di dati a **più dispositivi** di rete contemporaneamente

---

I [[Router|router]] si occupano di creare le [[Coppia|coppie]] di indirizzi necessarie
Gli indirizzi riservati iniziano generalmente coi bit `1110` quindi variano da `224.0.0.0` a `239.255.255.255` ma non vengono utilizzati molto e vengono spesso **bloccati**

In [[Indirizzo IPv6|IPv6]] l'indirizzo di multicast è `ff00::/8`