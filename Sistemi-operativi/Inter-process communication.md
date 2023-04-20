---
 Created: 2023-04-19 11:17
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [IPC]
 Tags: []
---

L'**inter-process communication** (o *IPC*) si riferisce all'insieme delle tecnologie [[Software|software]] il cui scopo è consentire a diversi [[Processo|processi]] di comunicare scambiandosi [[Dato|dati]] e [[Informazione|informazioni]]

---

Se due processi desiderano comunicare hanno bisogno di:
- Stabilire un **canale di comunicazione**
- **Inviare** messaggi attraverso un operazione di *send*
- **Ricevere** messaggi attraverso un operazione di *receive*

L'implementazione del canale di comunicazione può essere:
- **Fisica**: ad esempio tramite [[Memoria condivisa|memoria condivisa]] o tramite [[Hardware|hardware]] [[Bus|bus]]
- **Logica**: ad esempio tramite [[Messagge passing|message passing]]