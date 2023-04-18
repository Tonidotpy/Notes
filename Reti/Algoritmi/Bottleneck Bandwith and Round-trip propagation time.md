---
 Created: 2022-12-23 16:29
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [BBR]
 Tags: [algorithm]
---

**Bottleneck Bandwidth and Round-trip propagation time** (*BBR*) è una tecnica di **controllo** della congestione utilizzata in diverse tecnologie di rete per **gestire** il flusso di dati in modo da **evitare** il sovraccarico della rete e garantire una trasmissione efficiente dei dati

---

Il BBR è un algoritmo inventato da Google e si basa sulla **stima** di due parametri:
- La **banda** sul link *collo di bottiglia*
- L'[[Round Trip Time|RTT]]

É progettato per rispondere alla congestione effettiva piuttosto che alla perdita di pacchetti
É un algoritmo *server-side* ossia non richiede un'implementazione da parte del client

Rispetto a [[Convex hUll-Based Internet Congestion control|CUBIC]] garantisce:
- **Maggiore produttività**
- **Latenza inferiore**