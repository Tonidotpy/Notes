---
 Created: 2022-12-25 17:05
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Classful Addressing]
 Tags: []
---

L'**indirizzamento classful** è un metodo di **assegnazione** degli [[Indirizzo IPv4|indirizzi IP]] che viene utilizzato per dividere gli indirizzi in diverse classi in base ad un loro prefisso

---

É un tipo di indirizzamento **obsoleto** che suddivide gli IP in classi differenti con diverse lunghezze dei prefissi

>[!INFO] Il numero di indirizzi disponibili si esaurì in fretta con questo tipo di indirizzamento

| Classe | Prefisso | Bit per NetID | Bit per HostID | Numero di reti | Host per rete                   |
| ------ | -------- | ------------- | -------------- | -------------- | ------------------------------- |
| A      | `0`      | `7 bit`       | `24 bit`       | `128`          | `16777216`                      |
| B      | `10`     | `14 bit`      | `16 bit`       | `16384`        | `65536`                         |
| C      | `110`    | `21 bit`      | `8 bit`        | `2097152`      | `256`                           |
| D      | `1110`   | -             | -              | -              | `268435356` indirizzi multicast |
| E      | `1111`   | -             | -              | -              | `268435356` indirizzi non assegnati                              |