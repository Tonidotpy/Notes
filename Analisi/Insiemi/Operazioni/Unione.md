---
 Created: 2021-10-15 21:28
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [matematica,operazioni,analisi,insiemi]
---

# Unione

###### Definizione

Consideriamo l'insieme $A,\ B \subseteq E$ contenuti in un [[Insieme universo|insieme universo]] $E$.
L'**unione** è l'insieme contenente tutti gli elementi dell'insieme $A$ e tutti gli elementi dell'insieme $B$.

> $$A \cup B := \{x \in E\ |\ x \in A \lor x \in B\}$$

---

###### Caratteristiche

- L'**unione** di due o più insiemi si dice [[Intersezione#Proprietà|disgiunta]] se gli insiemi, presi a due a due, hanno [[Intersezione|intersezione]] vuota;

###### Proprietà

- L'**unione** è un'operazione [[Commutatività|commutativa]]: $A \cup B = B \cup A$;
- L'**unione** è un'operazione [[Associatività|associativa]]: $(A \cup B) \cup C = A \cup (B \cup C) = A \cup B \cup C$;
- L'**unione** è un'operazione [[Distributività|distributiva]] rispetto all'intersezione: $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$;
- Il [[Insiemi complementari|complementare]] dell'**unione** di due insiemi coincide con l'[[Intersezione|intersezione]] dei due [[Insiemi complementari|complementari]]: $(A \cup B)^C = A^C \cap B^C$;

---

- L'**unione** di qualsiasi insieme con l'[[Insieme vuoto|insieme vuoto]] coincide con l'insieme stesso: $A \cup \emptyset = A$;
- L'**unione** di due insiemi inscatolati $A,\ B \subseteq E$ con $A \subseteq B$ coincide con l'insieme più grande: $A \cup B = B$;
- L'**unione** di un insieme $A \subseteq E$ con un suo qualsiasi [[Insieme universo|insieme universo]] coincide con l'**insieme universo**: $A \cup E = E$;
- L'**unione** di un insieme con se stesso è l'insieme stesso: $A \cup A = A$;
- L'**unione** di due insiemi qualsiasi contiene entrambi gli insiemi: $A \subseteq A \cup B,\ B \subseteq A \cup B$;