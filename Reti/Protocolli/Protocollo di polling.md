---
 Created: 2022-12-30 15:54
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

Il **protocollo di polling** è un metodo di **accesso** al mezzo di trasmissione che viene utilizzato in alcune reti di comunicazione per **gestire** l'accesso al mezzo di trasmissione da parte di più dispositivi

---

Un nodo **master** *invita* gli altri nodi (**slave**) a trasmettere a turno
Viene utilizzato di solito se i dispositivi slave hanno **poche risorse**

I problemi del polling sono:
- I **messaggi di polling** che occupano il canale (*overhead*)
- La **latenza elevata**
- Un ***single point of failure*** (*master*) 