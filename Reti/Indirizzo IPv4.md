---
 Created: 2022-12-25 16:39
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Indirizzo IP, IPv4, IP]
 Tags: []
---

Un **indirizzo IP** è un numero **univoco** assegnato a ogni dispositivo di rete che viene utilizzato per **identificare** il dispositivo e per **instradare** i pacchetti di dati da e verso il dispositivo

---

L'indirizzo IP è una stringa di `32 bit` associata ad un'**interfaccia di rete**
Un'interfaccia di rete è una **connessione** tra il dispositivo e il collegamento fisico
Ogni indirizzo IP **pubblicamente** raggiungibile deve essere **unico**

Gli indirizzi IP vengono rappresentati come interi positivi a `8 bit` separati da punti
Perciò tutti gli IP disponibili si trovano all'interno del range `0.0.0.0` $\rightarrow$ `255.255.255.255`

---

Gli indirizzi IP sono generalmente divisi in due parti:
- **NetID**: un prefisso che identifica la rete alla quale l'host appartiene
- **HostID**: un suffisso che identifica un'interfaccia della rete specificata dall'NetID

Per la gestione di indirizzi IP fu istituita la **Internet Corporation for Assigned Names and Numbers** (*ICANN*) che a sua volta autorizza diverse entità, i *"registrar"*, ad assegnare blocchi di IP pubblici agli [[Internet Service Provider|ISP]]
Gli indirizzi IP vengono interpretati principalmente in 2 modi:
1. [[Indirizzamento Classful]]
2. [[Classless Inter-Domain Routing|CIDR]]

Quando un IP viene **confrontato** tra quelli delle reti raggiungibili se non trova alcuna corrispondenza viene indirizzato verso il [[Default Gateway]]

---

Gli indirizzi IP possono essere categorizzati in due tipi:
- [[Indirizzo IP pubblico|IP pubblici]]
- [[Indirizzo IP privato|IP privati]]

Esistono degli indirizzi IP **speciali** che non vengono mai assegnati agli host:
- [[Indirizzo di rete]]
- [[Directed Broadcast Address|Indirizzo di broadcast]] di una rete
- [[Limited Broadcast Address|Indirizzo di broadcast]] di una rete locale
- ***"Questo computer"***, ossia un IP con tutti i bit a `0` (`0.0.0.0`)
- [[Indirizzo di loopback]]
- [[Indirizzo di multicast]]
- [[Indirizzo link-local]]