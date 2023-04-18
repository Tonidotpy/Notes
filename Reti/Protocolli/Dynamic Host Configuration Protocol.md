---
 Created: 2022-12-27 17:37
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [DHCP]
 Tags: [protocol]
---

**Dynamic Host Configuration Protocol** (*DHCP*) è un protocollo di rete utilizzato per **assegnare** gli [[Indirizzo IPv4|indirizzi IP]] ai dispositivi di rete in modo **dinamico**

---

L'[[Host|host]] invia un messaggi **DHCP discover**, il server DHCP risponde con un messaggio **DHCP offer**, l'host richiede un indirizzo IP con un messaggio **DHCP request** che gli viene inviato dal server attraverso un messaggio **DHCP ack**

Il DHCP permette di **liberare** indirizzi quando questi non vengono utilizzati
Un IP "preso in prestito" (*lease*) rimane valido per un periodo **limitato** di tempo, una volta scaduto l'host può richiedere di **riutilizzare** lo stesso IP oppure di prenderne uno nuovo

Il DHCP internamente utilizza [[User Datagram Protocol|UDP]] principalmente per la sua **velocità** e perché DHCP è progettato per essere **robusto** a perdite e duplicati

Se non è presente alcun server DHCP si possono configurare gli IP **manualmente** oppure si imposta al client un indirizzo casuale di tipo [[Indirizzo link-local|link-local]] e si utilizza [[Address Resolution Protocol|ARP]] per cercare interfaccie con quell'indirizzo, se non si trova alcuna corrispondenza si può **utilizzare** l'indirizzo altrimenti si **ritenta** con lo stesso procedimento

## Messaggio DHCP

![DHCP-message|500](https://www.researchgate.net/publication/263813522/figure/fig10/AS:667882941866005@1536247110658/Packet-format-for-DHCP.png)

Un messaggio DHCP è formato da:
- **OP**: specifica se si tratta di una risposta o una richiesta
- **HTYPE**: specifica il tipo di hardware
- **HLEN**: specifica la lunghezza dell'indirizzo di livello 2
- **FLAGS**: specifica se il mittente può ricevere broadcast o risposte dirette
- **HOPS**: specifica quanti server hanno inoltrato la richiesta
- **XID**: si usa per far corrispondere le richieste alle risposte
- **SEC**: dice quanto tempo è passato da quando l'host si è attivato
- **YIADDR**: contiene l'indirizzo IP offerto al client DHCP
- **SIADDR**: contiene l'indirizzo IP del server DHCP
- **SNAME**: contiene il nome del server DHCP
- **GIADDR**: contiene l'IP di un [[Router|router]] di default

Eccetto il campo **OPTIONS** tutti gli altri campi hanno lunghezza fissa

Il DHCP può inviare anche informazioni su:
- Il nome e l'IP di un server [[Domain Name System|DNS]]
- La [[Subnet Mask|maschera di rete]] da utilizzare
- Informazioni di configurazione aggiuntive