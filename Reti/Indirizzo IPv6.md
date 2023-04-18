---
 Created: 2022-12-27 18:05
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [IPv6]
 Tags: []
---

Gli **indirizzi IPv6** sono [[Indirizzo IPv4|indirizzi IP]] a `128 bit` utilizzati per **identificare** i dispositivi all'interno di una rete

---

La notazione utilizzata per questo tipo di indirizzi è quella **esadecimale**, per `128 bit` ogni gruppo di `4 bit` viene scritto con una **cifra** per un totale di 32 cifre esadecimali per ogni indirizzo, in 8 gruppi da 4 cifre
I vari gruppi vengono separati da i due punti, ad esempio `2a03:2880:f108:0083:0000:0000:0000:25de`

Si possono **omettere** tutti gli zeri all'inizio di un campo, ad esempio `2a03:2880:f108:83:0:0:0:25de`

I gruppi consecutivi di zeri si rappresentano con un `::` ma si può usare solo una volta sul gruppo più lungo, ad esempio `2a03:2880:f108:0083::25de`

---

I **prefissi** e le **sottoreti** funzionano allo stesso modo del [[Classless Inter-Domain Routing|CIDR]] inclusa la notazione per la [[Subnet Mask|maschera di rete]]

Gli indirizzi **speciali** in IPv6 sono:
- ***"Questo computer"***, ossia un IP con tutti i bit a `0` (`::/128`)
- [[Indirizzo di loopback]]
- [[Indirizzo di multicast]]
- [[Indirizzo link-local]]