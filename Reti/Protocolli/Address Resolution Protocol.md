---
 Created: 2022-12-26 18:09
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [ARP]
 Tags: [protocol]
---

L'**Address Resolution Protocol** (*ARP*) è un protocollo di rete utilizzato per tradurre gli [[Indirizzo IPv4|indirizzi IP]] in [[Indirizzo MAC|indirizzi MAC]]

---

Nell'ARP l'[[Host|host]] che richiede di sapere l'indirizzo MAC di un altro host manda una richiesta a tutti gli host in quella rete e l'host con quell'indirizzo risponderà al mittente della richiesta

L'ARP viene utilizzato solo per comunicazioni *punto-punto* all'interno della **stessa rete**
É possibile utilizzare ARP anche con host di altre reti attraverso un [[Server proxy|proxy]] ARP che fa da intermediario fra le due reti

## Messaggio ARP

![ARP-message|400](https://reaper81.files.wordpress.com/2010/07/arp-header3.png?w=300&h=173)

I messaggi ARP vengono interpretati come **dati** da trasportare e **incapsulati** nel *payload* di un *frame*

Per evitare di inviare un messaggio per ogni datagramma le risposte ARP ricevute vengono salvate in **cache**
Le nuove risposte **sovrascrivono** quelle vecchie in cache che vengono **cancellate periodicamente** (ogni 30 secondi circa)