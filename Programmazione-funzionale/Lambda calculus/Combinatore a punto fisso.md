---
 Created: 2022-06-19 13:44
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Combinatore a punto fisso
I **combinatori a punto fisso** permettono di utilizzare la **ricorsione** senza esplicitarla.

Alcuni tipi di **combinatori** sono:
- [[Y combinatore|Y-combinatori]];
- $Z$-combinatori: $\lambda f.((\lambda x.(f (\lambda y.(xx)y)))(\lambda x.(f (\lambda y.(xx)y))))$;
- $H$-combinatori: $\lambda f.((\lambda x.xx)(\lambda x.(f (\lambda y.(x\lambda )y))))$.