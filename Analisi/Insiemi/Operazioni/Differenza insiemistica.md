---
 Created: 2021-10-17 20:25
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Differenza]
 Tags: [matematica,operazioni,analisi,insiemi]
---

# Differenza insiemistica

###### Definizione

La differenza tra due insiemi $A,\ B \subseteq E$ contenuti in un [[Insieme universo|insieme universo]] $E$ è per definizione l'operazione che sottrae agli elementi del primo insieme quelli del secondo.

> $$A - B := \{x \in A\ |\ x \notin B\}$$

---

###### Caratteristiche

- La differenza insiemistica può essere definita anche mediante le nozioni di [[Insiemi complementari|insieme complementare]] e [[Intersezione|intersezione]]: $A - B = A \cap B^C$;

###### Proprietà

- La **differenza insiemistica** non è *in generale* un'operazione [[Commutatività|commutativa]];

---

- La **differenza** tra un insieme e l'[[Insieme vuoto|insieme vuoto]] è uguale all'insieme stesso: $A - \emptyset = A$
- Viceversa la **differenza** tra l'[[Insieme vuoto|insieme vuoto]] e un qualsiasi altro insieme è uguale all'[[Insieme vuoto|insieme vuoto]]: $\emptyset - A = \emptyset$;
- La **differenza** tra un insieme $A \subseteq E$ e un suo sovrainsieme $B \subseteq E,\ A \subseteq B$ è uguale all'[[Insieme vuoto|insieme vuoto]]: $A - B = \emptyset$;
- La **differenza** tra un insieme $A \subseteq E$ e un suo qualsiasi [[Insieme universo|insieme universo]] $E$ è uguale all'[[Insieme vuoto|insieme vuoto]]: $A - E = \emptyset$;
- Viceversa la **differenza** tra un [[Insieme universo|insieme universo]] $E$ e un suo [[Sottoinsiemi|sottoinsieme]] $A \subseteq E$ è il [[Insiemi complementari|complementare]] dell'insieme stesso: $E - A = A^C$;
- La **differenza** tra un insieme $A$ e se stesso è uguale all'[[Insieme vuoto|insieme vuoto]]: $A - A = \emptyset$;
- La **differenza** tra due [[Intersezione#Proprietà|insiemi disgiunti]] $A,\ B \subseteq E$ è uguale al primo insieme della differenza: $A - B = A,\ B - A = B$;
- La differenza tra due insiemi $A,\ B \subseteq E$ è un [[Sottoinsiemi|sottoinsieme]] del primo insieme: $A - B \subseteq A,\ B - A \subseteq B$;