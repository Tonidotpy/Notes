---
 Created: 2021-11-08 15:12
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Complementare]
 Tags: [matematica,analisi,insiemi]
---

# Insiemi complementari

###### Definizione

Dato un **insieme** $A \subseteq E$ [[Sottoinsiemi|sottoinsieme]] di un [[Insieme universo|insieme universo]] $E$, si definisce **insieme complementare** di $A$ l'insieme degli elementi di $E$ che **non** appartengono ad $A$.

> $$A^C := \{x \in E\ |\ x \notin A\}$$

---

###### Caratteristiche

- Il **complementare** dell'[[Insieme vuoto|insieme vuoto]] è l'[[Insieme universo|insieme universo]]: $\emptyset^C = E$;
- Il **complementare** dell'[[Insieme universo|insieme universo]] è l'[[Insieme vuoto|insieme vuoto]]: $E^C = \emptyset$;
- Il **complementare** del complementare di un insieme $A$ è uguale ad $A$: $(A^C)^C = A$;
- La [[Differenza insiemistica|differenza]] tra l'[[Insieme universo|insieme universo]] e un insieme $A$ è il suo **complementare**: $A^C = E - A$;
- Il **complementare** dell'[[Intersezione|intersezione]] di due insiemi equivale all'[[Unione|unione]] dei complementari dei due insiemi: $(A \cap B)^C = A^C \cup B^C$;
- Il **complementare** dell'[[Unione|unione]] di due insiemi equivale all'[[Intersezione|intersezione]] dei complementari dei due insiemi: $(A \cup B)^C = A^C \cap B^C$;