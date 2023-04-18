---
 Created: 2022-12-25 14:49
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **router** è un dispositivo di rete che viene utilizzato per **instradare** i pacchetti di dati tra diverse reti o sottoreti

---

Si può dividere logicamente un router in:
- **Data plane**: è una funzione **locale** a ogni router che determina come inoltrare un datagramma da una porta di arrivo ad una di uscita e si occupa perciò del *forwarding*
- **Control plane**: è una logica **globale** della rete che determina come instradare un datagramma in un percorso tra due punti e si occupa perciò del *routing*

Per **instradare** i messaggi verso le destinazioni corrette un router utilizza una [[Tabella di Routing|tabella di routing]] per tenere traccia dei possibili percorsi

Un router è composto da delle porte in **ingresso** e delle porte in **uscita**

## Porte di ingresso

Attraverso una porta di ingresso i messaggi vengono poi accodati in un **buffer di inoltro** e successivamente inviati all'uscita corretta grazie ad un **sistema di commutazione**

Esistono principalmente tre tipi di sistemi di commutazione:
- [[Commutazione a memoria]]
- [[Commutazione a bus]]
- [[Commutazione a matrice]]

Un commutatore più lento della velocità complessiva delle porte di ingresso causa accodamenti con conseguenti ritardi e perdite
Quando un datagramma accodato al primo posto della coda impedisce quelli successivi ad avanzare viene chiamato **Blocco *head-of-line*** (*HOL*)

## Porte di uscita

In una porta di uscita i messaggi che arrivano dal sistema di commutazione vengono aggiunti ad un **buffer di accodamento** e vengono man mano inviati attraverso la rete

Come per il buffer di inoltro anche quello di accodamento se arrivano più pacchetti di quelli che riesce ad inviare vengono causati dei ritardi e/o delle perdite

Per decidere quanta memoria utilizzare per i buffer viene utilizzata la seguente formula:
$$\frac{\text{RTT} \cdot C}{\sqrt{N}}$$
Dove:
- $\text{RTT}$ è il [[Round Trip Time]]
- $C$ è la **velocità** del link
- $N$ è il **numero** di flussi

## Scheduling

Per decidere quale pacchetto trasmettere su un link vengono utilizzati dei **metodi di *scheduling***
Un tipo di scheduling è quello **FIFO** (*First-In-First-Out*) ossia inviare i piacchetti in ordine di arrivo nella coda

Per decidere quali pacchetti scartare invece ci sono varie **politiche**:
- ***Tail drop***: scarto i pacchetti in arrivo
- ***Priority drop***: scarto o cancello basandomi su un livello di priorità
- ***Random drop***: scarto o cancello casualmente