---
 Created: 2022-12-22 16:59
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [RTO]
 Tags: []
---

Il **Retransmission TimeOut** (*RTO*) è un parametro utilizzato in diverse tecnologie di rete per gestire la **ritrasmissione** di pacchetti di dati in caso di **errore** o perdita di pacchetti durante la trasmissione

---

Il valore dell'RTO deve essere più grande dell'[[Round Trip Time|RTT]] e dare ai messaggi il tempo di ricevere la risposta senza rallentare troppo l'invio di pacchetti

Il valore dell'RTO si può stimare tramite la seguente formula:
$$\text{RTO}(t) = \text{EstimatedRTT}(t) + 4 \cdot \text{DevRTT}(t)$$
Dove:
- $t$ e un istante di tempo
- $\text{EstimatedRTT}(t)$ è l'RTT stimato al tempo $t$
- $\text{DevRTT}(t)$ è un valore che rappresenta di quanto $\text{SampleRTT}(t)$ si discosta da $\text{EstimatedRTT}(t)$ al tempo $t$

$\text{DevRTT}(t)$ si calcola con la seguente formula:
$$\text{DevRTT}(t) = (1 - \beta) \cdot \text{DevRTT}(t-1) + \beta \cdot |\text{SampleRTT}(t) - \text{EstimatedRTT}(t)|$$
Dove:
- $t$ è un istante di tempo
- $\text{DevRTT}(t-1)$ è il $\text{DevRTT}$ nell'istante $t-1$
- $\text{SampleRTT}(t)$ è una misura reale dell'RTT al momento $t$
- $\text{EstimatedRTT}(t)$ è una stima dell'RTT nel tempo $t$
- $\beta$ è un valore compreso tra `0` e `1`, tipicamente `0.25`