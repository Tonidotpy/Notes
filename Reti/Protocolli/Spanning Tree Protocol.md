---
 Created: 2022-12-30 18:20
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [STP]
 Tags: [protocol]
---

Lo **Spanning Tree Protocol** (*STP*) è un protocollo di rete utilizzato per **prevenire** i *loop* di rete, ovvero situazioni in cui un pacchetto di dati viene inviato in modo continuo in una rete senza mai raggiungere la sua destinazione

---

Ad ogni [[Switch Ethernet]] viene dato un identificatore da `64 bit` formato da:
- `16 bit` impostati dall'**amministratore di rete**
- `48 bit` composti dall'[[Indirizzo MAC|indirizzo MAC]] dello switch

STP costruisce un **albero** con radice nello switch che ha l'**ID** più basso

---

Gli switch si scambiano dei **pacchetti di controllo** chiamati **Bridge Protocol Data Unit** (*BPDU*) che contengono l'ID del mittente e il costo del link

Quando uno switch `A` riceve una BPDU da un altro switch `B` **controlla** gli ID e se il proprio ID è minore, la porta di `B` verso `A` diventa radice dell'albero per `B`
Altrimenti, la porta da cui `A` riceve la BPDU diventa radice dell'albero per `A` e `B` diventa un **progenitore** di `A`
`A` aggiorna il proprio costo alla somma dei costi tra `A` e `B`
Le porte da cui `A` riceve un BPDU con costo **minore** del proprio diventano *designated ports* (figli di `A` nell'albero), altrimenti se il costo è **uguale** diventano *blocked ports* (potenziali progenitori di `B` che creerebbero dei *loop*)

**Periodicamente** vengono inviate le BPDU  per rilevare dei cambiamenti nella topologia di rete, solamente attraverso le *desigated ports* e non attraverso quelle *blocked* che non vengono mai coinvolte nella trasmissione