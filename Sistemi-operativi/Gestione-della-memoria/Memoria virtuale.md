---
 Created: 2023-05-12 15:34
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

La **memoria virtuale** è un'**architettura di sistema** capace di simulare uno spazio in [[Memoria primaria|memoria centrale]] maggiore di quello fisicamente presente utilizzando la [[Memoria secondaria|memoria secondaria]]

---

>[!INFO] La [[Sistemi-operativi/Gestione-della-memoria/Partizione|partizione]] di **memoria secondaria** che viene utilizzata come parte della **memoria virtuale** viene chiamata [[Partizione di swap|swap]]

Tramite la memoria virtuale lo spazio occupato dai [[Processo|processi]] inutilizzati può essere trasferito sulla memoria secondaria liberando così effettivamente spazio nella memoria centrale

Esistono due tipi di implementazione della memoria virtuale:
1. [[Paginazione su domanda]]
2. [[Segmentazione su domanda]]