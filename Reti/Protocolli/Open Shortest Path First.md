---
 Created: 2022-12-28 15:53
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [OSPF]
 Tags: [protocol]
---

**Open Shortest Path First** (*OSPF*) è un protocollo di routing utilizzato per **instradare** i pacchetti di dati su Internet e sulle altre reti di [[Computer|computer]]

---

OSPF utilizza l'[[Algoritmo di Dijkstra|algoritmo di Dijkstra]] per calcolare il percorso più breve in cui spedire i pacchetti
Utilizza i datagrammi [[Internet Protocol versione 4|IP]] e invia i pacchetti di **aggiornamento** dei link all'[[Indirizzo di multicast|indirizzo multicast]] `224.0.0.5`

OSPF implementa **tre** procedure:
- **Protocollo di *"Hello"***: vengono inviati dei **messaggi di mantenimento** per verificare che i link siano funzionanti e quali nodi sono raggiungibili da un nodo
- **Protocollo di *"Exchange"***: viene utilizzato per informare i vicini che si sono appena "conosciuti" sulla topologia della rete nota al momento
- **Protocollo di *"Flooding"***: informa tutti i router di un cambio nello stato dei link

I messaggi di flooding possono essere inviati in modo **controllato** inoltrando tutti i messaggi ricevuti su un'interfaccia a tutte le altre solo se:
- Esistono solo **connessioni dirette** (reti con [[Subnet Mask]] `/30`) ad altri [[Router]] (viene inviato un messaggio per link)
- Oppure in reti con un [[Dominio di broadcast|dominio di broadcast]] (viene inviato un messaggio per dominio)

---

Per le reti con molti router conviene utilizzare l'**OSPF gerarchico**, ossia una versione del protocollo con una gerarchia a **due livelli**:
- **Dorsale** (*backbone*): un [[Autonomous System|AS]] radice connesso a tutte le altre aree di stub tramite dei **router di bordo**
- **Reti di area** (*stub*): AS connessi alla dorsale, in queste aree circolano i messaggi sugli stati dei link

I nodi conoscono solo la **topologia di rete** della propria area e il cammino più breve verso le altre aree, anche la dorsale conta come un'area
I router di bordo connettono la dorsale alle aree di stub utilizzando il protocollo [[Border Gateway Protocol|BGP]]