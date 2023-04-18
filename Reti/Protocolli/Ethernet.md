---
 Created: 2022-12-08 16:17
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

**Ethernet** è uno **standard** di rete che definisce le regole per la trasmissione dei dati su una **rete cablata**.

---

É uno dei [[Protocollo|protocolli]] di rete più diffusi al mondo e viene utilizzato specialmente per le [[Local Area Network|LAN]]
É un protocollo **non orientato alla connessione** (*connectionless*) e **non affidabile** nel senso che non tenta di recuperare frame persi tramite ritrasmissioni a meno che il metodo non venga implementato a livelli più alti

In base allo **standard** può raggiungere velocità  fino a `10 Mbit/s`, `100 Mbit/s`, `1 Gbit/s`, `10 Gbit/s`

---

Un **cavo ethernet** è un *doppino intrecciato* che può essere classificato in base al modo in cui è **schermato**:
- **U**: cavo non schermato (*unshielded*)
- **F**: cavo avvolto da una sottile lamina, solitamente di alluminio (*Foiled*)
- **S**: cavo avvolto da una maglia metallica intrecciata (*Shielded*)
- **SF**: una combinazione delle due precedenti

La denominazione dei cavi avviene nel formato `X / Y TP` dove `X` è la **schermatura dell'intero cavo** mentre `Y` è la **schermatura di ogni doppino**, quest'ultima può essere solo di tipo **U** o **F**

---

Lo **standart** Ethernet è lo `802.3` che venne per la prima volta implementato nel 1985

La prima tipologia di ethernet fu il **BUS**, un mezzo di trasmissione condiviso (ad accesso multiplo) a cui i dispositivi si potevano **collegare** per inviare o ricevere segnali tramite un **transceiver**

![Ethernet-10base5](https://rdv-files.nyc3.cdn.digitaloceanspaces.com/pub/html/files_html/3/5/2/000033520.png)

La seconda tipologia migliorava l'implementazione dei *transceiver* rendendoli più simili a delle schede di rete

![Ethernet-10base-2|500](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWYazwWkxZgo8l79W9fOUOmCadr2BYf0MCjw&usqp=CAU)

La svolta fu il passaggio dalla tecnologia bus a quella degli **HUB** (che possono essere sostituiti con degli [[Switch Ethernet]], ossia un ripetitore *multi-porta* che collegava tutti i dispositivi migliorando di gran lunga l'efficienza e la mantenibilità del sistema
Altri punti di svolta furono i **doppini incrociati** e i **connettori** RJ45 tuttora utilizzati

![Ethernet-connector-RJ45](https://upload.wikimedia.org/wikipedia/commons/e/ef/RJ-45_TIA-568B_Right.png)

---

## Frame Ethernet

^702d8e

Un frame ethernet è composto da:
- Un **preambolo** di `7 Bytes` con valore `10101010`
- Uno **Start Frame Delimiter** di `1 Byte` con valore `10101011` utilizzato per **sincronizzare** il clock del ricevitore e del trasmettitore
- L'**[[Indirizzo MAC|indirizzo MAC]] di destinazione** di `6 Byte` che se non corrisponde al dispositivo corrente o ad un [[Limited Broadcast Address|indirizzo di broadcast]] fa scartare l'intero frame
- L'**indirizzo MAC sorgente** di `6 Byte`
- La **lunghezza** del frame di `2 Byte`
- Il [[Cyclic Redundancy Check|CRC]] per rilevare errori all'interno del frame di `4 Byte`

![Ethernet-802.3-frame](https://www.gatevidyalay.com/wp-content/uploads/2018/10/Ethernet-Frame-Format-IEEE-802.3.png)