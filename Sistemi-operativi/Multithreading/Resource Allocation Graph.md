---
 Created: 2023-05-01 17:22
 Author: Antonio Gelain
 Aliases: [RAG]
 Tags: [multithreading]
---

Un **resource allocation graph** (in breve *RAG*) è un modello astratto per la determinazione e la rappresentazione di eventuali situazioni di [[Deadlock|deadlock]]

---

RAG è un [[Grafo|grafo]] $G(V,E)$ dove:
- L'[[Insiemi|insieme]] di **nodi** $V$ rappresenta i [[Processo|processi]] (indicati come cerchi) e le **risorse** (indicate come **quadrati**)
- L'insieme di **archi** $E$ da processo a risorsa rappresenta la richiesta della risorsa da parte di quel processo, mentre da risorsa a processo indica che tale risorsa è detenuta da quel processo

Se il RAG non contiene [[Ciclo|cicli]], non ci sono **deadlock**, altrimenti:
- Se si ha **una sola istanza** per risorsa allora è presente un *deadlock*
- Se sono presenti **più istanze**, dipende dallo schema di allocazione