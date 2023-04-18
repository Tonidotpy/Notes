---
 Created: 2022-12-10 17:32
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **protocollo** è un insieme di **regole** e di **convenzioni** che definiscono come le diverse parti di un **sistema** di comunicazione devono **interagire** tra loro

---

Per la comunicazione dei dati in una rete sono stati stabiliti dei **modelli di riferimento** composti da un insieme di protocolli suddivisi su più **livelli**:
1. La [[Pila ISO-OSI|pila ISO/OSI]], più vecchia è composta da **sette** strati
2. La [[Pila TCP-IP|pila TCP/IP]], più recente è composta da **cinque** (o *quattro*?) strati

Ogni strato (*layer*) fornisce **servizi** al livello superiore attraverso servizi del livello inferiore e le proprie funzionalità
I serivizi vengono forniti attraverso i **Service Access Point** (*SAP*) regolandone lo scambio proprio tramite un protocollo

In un sistema con $M$ layer i dati da trasmettere costituiscono un **Service Data Unit** (*SDU*) di layer $M$
A ciò il layer aggancia la propria **Protocol Control Information** (*PCI*) formando così una **Protocol Data Unit** (*PDU*) ^b551b1

![PDU-encapsulation|350](https://www.oreilly.com/api/v2/epubs/9781789340501/files/assets/4413e8e2-d953-4431-af99-1f96ce07e8b4.png) ^7f3982

Perciò una **PDU** al livello $N$ non è altro che la **SDU** di livello $N-1$ più la **PCI** del livello $N$