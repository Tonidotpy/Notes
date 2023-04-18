---
 Created: 2022-12-21 16:51
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il **pipelining** è una tecnica utilizzata nei protocolli di rete per aumentare l'**efficienza** del **trasferimento** dei dati
Consiste nell'inviare più **richieste** o comandi di seguito, senza attendere la risposta a ciascuno di essi prima di inviare il successivo

---
Nel pipelining un trasmettitore accetta che ci siano diversi **pacchetti** *"in volo"* però:
- Va tenuta **traccia** dei numeri di sequenza dei pacchetti *"in volo"*
- Bisogna memorizzare i segmenti sia al trasmettitore sia al ricevitore