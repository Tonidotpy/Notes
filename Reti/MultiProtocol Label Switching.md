---
 Created: 2022-12-31 17:39
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [MPLS]
 Tags: []
---

**Multiprotocol Label Switching** (*MPLS*) è una tecnologia di rete utilizzata per **fornire** una connessione di rete **veloce** e **affidabile** per il traffico di dati

---

Per implementare l'MPLS viene aggiunto un **header** tra l'[[Internet Protocol versione 4#Datagramma IP|header IP]] e quello [[Ethernet#Frame Ethernet|Ethernet]]

![MPLS-frame-header](https://miro.medium.com/max/485/1*Umdp5m0NBwWmMx8TbcaJfw.png)

Il concetto è lo stesso del routing IP ma è più **veloce** e offre diverse alternative per raggiungere la stessa destinazione
L'header MPLS **incapsula** il datagramma IP nascondendone gli [[Indirizzo IPv4|indirizzi]] perciò permette di creare [[Virtual Private Network|VPN]], di colegare terminali con [[Indirizzo IP privato|indirizzi privati]] e indirizzi per cui non esistono regole di routing