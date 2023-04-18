---
 Created: 2022-12-30 17:50
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Uno **switch Ethernet** è un dispositivo di rete utilizzato per **connettere** più dispositivi di rete insieme in modo da consentire loro di **comunicare** tra loro

---

Uno swith memorizza ed **inoltra** il [[Ethernet#Frame Ethernet|frame ethernet]] ed **esamina** l'[[Indirizzo MAC|indirizzo MAC]]
Uno switch risulta **trasparente** a tutti i dispositivi collegati ed è di tipo *Plug-and-Play*, ossia non ha bisogno di essere esplicitamente configurato

All'interno di una rete *"switched"* ogni dispositivo ha un **canale dedicato** per comunicare con lo switch dove viene utilizzato il protocollo [[Ethernet]]
Gli unici nodi ad usarlo sono il dispositivo e lo switch, in questo modo si evitano **collisioni** in *full duplex* e ogni link è un [[Dominio di collisione|dominio di collisione]] a parte

---

Per sapere quale interfaccia è collegata ad un certo dispositivo, uno switch utilizza una **tabella** che viene mantenuta utilizzando l'**autoapprendimento** (*backward learning*)

Alla ricezione di un frame, lo switch aggiorna la tabella **annotando** la porta da cui proviene e l'indirizzo MAC del dispositivo e controlla se ha le informazioni per raggiungere il destinatario, nel caso in cui non le trovi **inoltra** il messaggio a tutte le interfacce

Questo tipo di **autoapprendimento** funziona anche con topologie della rete più complesse

All'interno delle topologie di rete che utilizzano degli switch bisogna **evitare** di creare *loop* in quanto permettono al metodo di autoapprendimento di **saturare** la capacità dei link e **sovraccaricare** gli apparati
Nel caso in cui non si possa (o non si voglia) evitare di creare dei **cicli** si può utilizzare lo [[Spanning Tree Protocol|STP]]