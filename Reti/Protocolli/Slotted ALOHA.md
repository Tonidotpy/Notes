---
 Created: 2022-12-29 19:51
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

Lo **Slotted ALOHA** è una variante del protocollo [[ALOHA]] che viene utilizzata in alcune reti di comunicazione per **gestire** l'accesso al mezzo di trasmissione da parte di più dispositivi

---

Si assume che tutti i pacchetti (*frame*) abbiano la **stessa lunghezza** e che il tempo sia suddiviso in *slot*, ciascuno lungo quanto un pacchetto
I nodi possono trasmettere solo all'inizio di uno slot e sono **sincronizzati** permettendo così di rilevare una **collisione**

Quando un nodo ha qualcosa da inviare lo invia nello slot **immediatamente successivo** e se non ci sono collisioni continua a trasmettere anche in quello **seguente**
Se c'è una **collisione** il nodo ritrasmette il pacchetto con **probabilità** `p` in ogni slot seguente finché non ha **successo**

---

| Vantaggi                                                                       | Svantaggi                                                                      |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| Se un solo nodo è attivo, può usare il canale **continuamente**                | Le **collisioni** sono probabili e sprecano risorse                            |
| Il protocollo è **decentralizzato** e serve solo **sincronizzarsi** sullo slot | Gli slot potrebbero rimanere **vuoti**                                         |
| É un protocollo molto **semplice**                                             | Si potrebbe rilevare la collisione senza aspettare la fine di una trasmissione |
|                                                                                | Sincronizzarsi richiede coordinamento                                                                               |