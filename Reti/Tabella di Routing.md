---
 Created: 2022-12-26 15:56
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Una **tabella di routing** è una **lista di percorsi** utilizzata da un [[Router|router]] o da un altro dispositivo di rete per **instradare** i pacchetti di dati verso i loro destinatari

---

All'interno della tabella di routing vengono memorizati gli **[[Indirizzo IPv4|IP]] di destinazione** e le loro **interfaccie di rete** collegate
Se l'IP di destinazione non è raggiungibile direttamente viene incluso anche l'IP del router a cui **inoltrare** il messaggio in modo che possa raggiungere la sua destinazione

Il **data plane** si occupa di leggere la tabella e trovare l'interfaccia e il destinatario a cui inviare il pacchetto
Il **control plane** si occupa di poplare la tabella inserendo tutti i dati su gli indirizzi IP raggiungibili direttamente

Esistono diversi algoritmi che permettono di **popolare dinamicamente** la tabella di routing:
- [[Algoritmo di Dijkstra]]
- [[Algoritmo di Bellman-Ford]]