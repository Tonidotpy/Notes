---
 Created: 2023-04-18 10:28
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **context switching** è un operazione che conserva lo stato di un [[Processo|processo]] o [[Thread|thread]] in modo da poter essere ripreso in un altro momento

---

Durante questa operazione viene salvato il [[Process Control Block|PCB]] del processo uscente e caricato quello del processo entrante
Purtroppo questa operazione è **molto costosa** e richiede tempo perciò se viene eseguita troppo spesso rischia di ridurre le prestazioni del [[Computer|computer]]