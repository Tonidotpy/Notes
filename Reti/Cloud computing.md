---
 Created: 2022-12-12 19:46
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **cloud computing** è un modello di informatica che consente l'accesso a **risorse** informatiche, come calcolo, archiviazione, rete e software, attraverso [[Internet]]

---

La creazione di una **copia** di sicurezza dei dati (*backup*) è **automatica**
I dati vengono memorizzati in *server farm* ad alta affidabilità generalmente localizzate presso i *data center* degli [[Internet Service Provider|ISP]]

Il fornitore dei servizi espone delle interfacce per elencare e gestire i propri servizi

Le **criticità** di questo sistema sono principalmente:
- **Sicurezza** e **privacy** dal momento che i dati non sono accessibili direttamente e non è possibile conoscerne la posizione fisica
- Problemi di natura **economico/politica**
- **Continuità** del servizio offerto
- **Difficoltà di migrazione** dei dati

---

Un *cloud data center* è formato da:
- **Core network**: un livello che si interfaccia con la rete internet
- **Aggregation network**: un livello che si frappone fra il core network e il livello di accesso
- **Access network**: il livello che si occupa di accedere fisicamente ai dati richiesti

![cloud-data-center](https://benchpartner.com/wp-content/uploads/2020/04/Architectural-Design-of-Data-Centers-in-Cloud-Computing.png)