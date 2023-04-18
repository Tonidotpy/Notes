---
 Created: 2022-12-31 17:17
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Virtual LAN, VLAN]
 Tags: []
---

La **Virtual Local Area Network** (*VLAN*) è una tecnologia di rete utilizzata per creare **reti virtuali** all'interno di una rete fisica

---

Una VLAN è formata da un **insieme di porte** di uno o più [[Switch Ethernet|switch di rete]] che possono supportare VLAN multiple (se le VLAN vengono supportate)

Gli switch eseguono un processo di *backward learning* **indipendente** per ogni VLAN e il broadcast avviene solamente all'interno della VLAN da cui è stato inviato il pacchetto

---

Non è necessario che tutti i dispositivi appartenenti ad una VLAN siano connessi allo stesso switch di rete però questo porta alla possibilità di avere *link* che devono trasportare del traffico di diverse VLAN, le porte che fanno parte di questo collegamento vengono chiamate ***trunk***

Per poter utilizzare le VLAN su switch multipli fu stabilito un nuovo **standart** [[Ethernet]], l'`802.1Q` che aggiunge al messaggio del protocollo precedente:
- **TPID** `2 Byte`: l'ID del protocollo VLAN con un valore fissato a `0x8100`
- **User Priority** `3 bit`: la priorità del frame
- **Canonical Format Indicator** (*CFI*) `1 bit`: inizialmente specificava se l'ordine dei byte era [[Big Endian]] o [[Little Endian]]
- **VLAN ID** `12 bit`: un identificatore per le VLAN (`0` se non presente), `0xFFF` è un valore **riservato**

![Ethernet-802.1Q-frame](https://www.researchgate.net/publication/330313553/figure/fig2/AS:713938312392705@1547227566692/IEEE-8021q-tagged-Ethernet-frame.png)

Questo standard è **retrocompatibile** anche con gli switch ethernet che non supportano le VLAN