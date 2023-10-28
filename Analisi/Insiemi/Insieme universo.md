---
 Created: 2021-10-19 09:33
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Insieme ambiente]
 Tags: [matematica,analisi,insiemi]
---

# Insieme universo

###### Definizione

Chiamiamo **insieme universo**, o **insieme ambiente**, di un insieme $A$ un qualsiasi insieme che contiene $A$ come [[Sottoinsieme|sottoinsieme proprio o improprio]].

> $$U \text{ insieme universo di } A \iff A \subseteq U$$

---

###### Caratteristiche

- Il [[Insiemi complementari|complementare]] dell'**insieme universo** è uguale all'[[Insieme vuoto|insieme vuoto]]: $U^C = \emptyset$;

###### Proprietà

- L'[[Unione|unione]] tra un insieme $A \subseteq U$ e un suo qualsiasi **insieme universo** $U$ è uguale all'insieme unverso $U$: $A \cup U = U$;
- L'[[Intersezione|intersezione]] tra un insieme $A \subseteq U$ e un suo qualsiasi **insieme universo** $U$ è uguale all'insieme $A$: $A \cap U = A$;
- La [[Differenza insiemistica|differenza]] tra un insieme $A \subseteq U$ e un suo qualsiasi insieme universo $U$ è uguale all'[[Insieme vuoto|insieme vuoto]]: $A - U = \emptyset$;
- Al contrario la [[Differenza insiemistica|differenza]] tra un **insieme universo** $U$ di un insieme $A$ e l'insieme $A$ è uguale al [[Insiemi complementari|complementare]] dell'insieme $A$ in $U$: $U - A = A^C$;
- La [[Differenza simmetrica|differenza simmetrica]] tra un insieme $A \subseteq U$ e un suo qualsiasi **insieme universo** $U$ è uguale al [[Insiemi complementari|complementare]] di $A$ in $U$: $A \Delta U = A^C$;
- Il [[Insiemi complementari|complementare]] di un insieme $A$ si riferisce per definizione all'**insieme universo** in cui si considera $A$, ed è definito come l'insieme degli elementi di $U$ che **non** appartengono ad $A$: $A \subseteq U,\ A^C = \{x \in U\ |\ x \notin A\}$;