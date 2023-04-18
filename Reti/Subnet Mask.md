---
 Created: 2022-12-25 17:29
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Maschera di Rete]
 Tags: []
---

Una **Subnet Mask** è una sequenza di numeri binari che viene utilizzata per **definire** le parti di un [[Indirizzo IPv4|indirizzo IP]] che rappresentano la rete e gli host

---

La subnet mask è formata da `32 bit` in cui gli unici bit a `1` sono quelli del **prefisso**
Come per gli indirizzi IP la maschera di rete viene rappresentata da numeri interi positivi a `8 bit` separati da dei punti

Nella maschera di rete i bit posti a `1` devono **iniziare** dalla cifra più significativa e devono essere **adiacenti** tra di loro ossia non possono essere separati da degli zeri

> [!SUCCESS] **Subnet Mask valida**: `11111111.11111111.11000000.00000000`

> [!FAILURE] **Subnet Mask non valida**: `11111111.11101111.11000000.00000000`
