---
 Created: 2022-12-27 18:10
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [IPv6]
 Tags: [protocol]
---

L'**Internet Protocol versione 6** (*IPv6*) è la versione successiva dell'[[Internet Protocol versione 4|IP]] il protocollo di rete utilizzato per **instradare** i pacchetti di dati su una rete di [[Computer|computer]]

---

Questo protocollo fu inizialmente creato per **ampliare** la quantità di indirizzi disponibili, **velocizzare** l'elaborazione dei datagrammi e **facilitare** la gestione della qualità del servizio

Per gestire la graduale transizione da IPv4 i datagrammi IPv6 vengono **incapsulati** all'interno dei datagrammi IPv4 (*tunneling*)

## Datagramma IPv6

La lunghezza dell'header viene **fissata** esattamente a `40 Byte` e la frammentazione viene **proibita**

![IPv6-datagram|450](http://www-inf.telecom-sudparis.eu/~hennequi/CoursIP6/A19.jpeg)

**Flow label** è un etichetta per tutti i datagrammi all'interno dello stesso **flusso** (anche se il concetto di flusso non è ben definito)
La *Traffic Class* è la **priorità** dei datagrammi che fanno parte dello stesso flusso
**Next header** identifica il protocollo di livello 4 **incapsulato nei dati**

In IPv6 la **checksum** e le **options** vengono rimosse e vengono aggiunti dei messaggi di errore (ad esempio *Packet Too Big*)  e funzione di gestione per i gruppi multicast

Gli [[Indirizzo IPv6|indirizzi IPv6]] hanno una lunghezza maggiore (`128 bit`) rispetto a quelli di IPv4 (`32 bit`)