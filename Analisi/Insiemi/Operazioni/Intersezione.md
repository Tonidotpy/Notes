---
 Created: 2021-10-15 22:09
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [matematica,operazioni,analisi,insiemi]
---

# Intersezione

###### Definizione

Consideriamo due insiemi $A,\ B \subseteq E$ contenuti in un [[Insieme universo|insieme universo]] $E$.
Definiamo l'**intersezione** tra gli insiemi $A$ e $B$ come l'insieme degli elementi appartenenti a entrambi gli insiemi, ossia degli elementi in comune tra di essi.

> $$A \cap B := \{x \in E\ |\ x \in A \land x \in B\}$$

---

###### Proprietà

- L'**intersezione** è un'operazione [[Commutatività|commutativa]]: $A \cap B = B \cap A$;
- L'**intersezione** è un'operazione [[Associatività|associativa]]: $(A \cap B) \cap C = A \cap (B \cap C) = A \cap B \cap C$;
- L'**intersezione** è un'operazione [[Distributività|distributiva]] rispetto all'unione: $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$;
- L'**intersezione** è un'operazione [[Distributività|distributiva]] rispetto alla [[Differenza simmetrica|differenza simmetrica]] tra insiemi: $A \cap (B \Delta C) = (A \cap B) \Delta (A \cap C)$;
- Il [[Insiemi complementari|complementare]] dell'**intersezione** di due insiemi coincide con l'[[Unione|unione]] dei due [[Insiemi complementari|complementari]]: $(A \cap B)^C = A^C \cup B^C$;

---

- L'**intersezione** di un qualsiasi insieme con l'[[Insieme vuoto|insieme vuoto]] è uguale all'[[Insieme vuoto|insieme vuoto]]: $A \cap \emptyset = \emptyset$;
- L'**intersezione** di due insiemi inscatolati $A,\ B \subseteq E$ con $A \subseteq B$ coincide con l'insieme che è contenuto nell'altro: $A \cap B = A$;
- L'**intersezione** di un insieme $A \subseteq E$ con un suo qualsiasi [[Insieme universo|insieme universo]] è uguale all'insieme stesso: $A \cap E = A$;
- L'**intersezione** di un insieme con se stesso è l'insieme stesso: $A \cap A = A$;
- Se due insiemi $A,\ B \subseteq E$ non hanno elementi in comune hanno un'**intersezione vuota** e vengono chiamati **insiemi disgiunti**: $A \cap B = \emptyset$;
- L'**intersezione** di due insiemi qualsiasi è un [[Sottoinsiemi|sottoinseme]] di entrambi gli insiemi: $A \cap B \subseteq A,\ A \cap B \subseteq B$;