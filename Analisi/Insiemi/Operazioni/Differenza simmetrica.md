---
 Created: 2021-10-18 14:36
 Author: Antonio Gelain
 Aliases: []
 Tags: [matematica,operazioni,analisi,insiemi]
---

# Differenza simmetrica

###### Definizione

La **differenza simmetrica** $\Delta$ tra due insiemi $A,\ B \subseteq E$ contenuti in un [[Insieme universo|insieme universo]] $E$ equivale all'[[Unione|unione]] tra i due insiemi [[Differenza insiemistica|differenza]].

> $$A \Delta B := (A - B) \cup (B - A)$$
> $$A \Delta B := \{(x \in A \land x \notin B) \lor (x \in B \land x \notin A)\}$$
> $$A \Delta B = (A \cup B) - (A \cap B)$$

---

###### Proprietà

- La **differenza simmetrica** gode della [[Commutatività|proprietà commutativa]]: $A \Delta B = B \Delta A$;
- La **differenza simmetrica** gode della [[Associatività|proprietà associativa]]: $(A \Delta B) \Delta C = A \Delta (B \Delta C)$;
- La **differenza simmetrica** tra differenze simmetriche è uguale alla differenza simmetrica tra il primo elemento della prima differenza e il secondo della seconda: $(A \Delta B) \Delta (B \Delta C) = A \Delta C$;
- L'[[Intersezione|intersezione]] tra insiemi è una [[Distributività|proprietà distributiva]] rispetto alla **differenza simmetrica**: $A \cap (B \Delta C) = (A \cap B) \Delta (A \cap C)$;

---

- La **differenza simmetrica** di un insieme con se stesso è l'[[Insieme vuoto|insieme vuoto]]: $A \Delta A = \emptyset$;
- La **differenza simmetrica** tra due [[Intersezione#Proprietà|insiemi disgiunti]] $A,\ B \subseteq E$ contenuti in un insieme universo $E$ coincide con l'[[Unione|unione]] degli stessi: $A \Delta B = A \cup B$;
- La **differenza simmetrica** di un insieme $A$ con l'insieme vuoto è uguale all'insieme stesso: $A \Delta \emptyset = A$;