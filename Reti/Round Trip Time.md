---
 Created: 2022-12-22 17:04
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [RTT]
 Tags: []
---

ll **Round Trip Time** (*RTT*) è un parametro di rete che indica il **tempo** necessario per **inviare** un pacchetto di dati da un punto A a un punto B e **ricevere** una risposta
In altre parole, l'RTT rappresenta il tempo di **andata** e **ritorno** di un pacchetto di dati tra due punti di una rete

---

Per stimare l'RTT si può guardare in media quanto tempo impiegano i pacchetti per ricevere una risposta all'interno di una rete in condizioni *"normali"*, generalmente si utilizza la seguente formula:
$$\text{EstimatedRTT}(t) = (1 - \alpha) \cdot \text{EstimatedRTT}(t-1) + \alpha \cdot \text{SampleRTT}(t)$$
Dove:
- $\alpha$ è un valore compreso fra `0` e `1`, generalmente `0.125`
- $t$ è il numero che rappresenta un istante di tempo
- $SampleRTT(t)$ è una misura reale dell'RTT al momento $t$
- $EstimatedRTT(t-1)$ è l'RTT stimato nel momento $t-1$