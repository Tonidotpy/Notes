---
 Created: 2021-10-18 15:33
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [matematica,operazioni,analisi,insiemi]
---

# Prodotto cartesiano

###### Definizione

Consideriamo due insiemi $A,\ B \subseteq E$ contenuti in un [[Insieme universo|insieme universo]] $E$.
Chiamiamo **prodotto cartesiano** tra gli insiemi $A$ e $B$ l'insieme che ha per elementi tutte le possibili [[Coppia|coppie ordinate]] $(a, b)$ con $a \in A$ e $b \in B$.

> $$A \times B := \{(a, b)\ |\ a \in A,\ b \in B\}$$

---

###### Caratteristiche

- Il **prodotto cartesiano** può essere esteso anche a 3 o più insiemi e nel caso di $n$ insiemi esso avrà come elementi delle [[N-uple|n-uple ordinate]]: $A_1 \times A_2 \times ... \times A_n = \{(a_1, a_2, ..., a_n)\ |\ a_1 \in A_1,\ a_2 \in A_2,\ ...\ a_n \in A_n\}$;

###### Proprietà

- Il **prodotto cartesiano** tra due insiemi $A,\ B \subseteq E$ contenuti in un [[Insieme universo|insieme universo]] $E$ non gode della [[Commutatività|proprietà commutativa]];
- Il **prodotto cartesiano** gode della [[Distributività|proprietà distributiva]] rispetto all'[[Unione|unione]]: $A \times(B \cup C) = (A \times B) \cup (A \times C)$;
- Il **prodotto cartesiano** gode della [[Distributività|proprietà distributiva]] rispetto all'[[Intersezione|intersezione]]: $A \times(B \cap C) = (A \times B) \cap (A \times C)$;

---

- Il **prodotto cartesiano** di un insieme qualsiasi e l'[[Insieme vuoto|insieme vuoto]] è l'[[Insieme vuoto|insieme vuoto]]: $A \times \emptyset = \emptyset,\ \emptyset \times A = \emptyset$;
- Se $A$ è un insieme di [[Insiemi#Simboli|cardinalità]] $n$ e $B$ è un insieme di [[Insiemi#Simboli|cardinalità]] $m$ allora la [[Insiemi#Simboli|cardinalità]] del loro **prodotto cartesiano** è $n \times m$: $|A| = n,\ |B| = m \Rightarrow |A \times B| = n \times m$;