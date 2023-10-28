---
Created: 2022-03-03 08:39
Author: Antonio Gelain
aliases: 
tags:
  - matematica
  - analisi
  - insiemi
---

# Relazione

Una **relazione** $R$ tra due [[Analisi/Insiemi/Insieme|insiemi]] $A$ e $B$ è un [[Sottoinsieme|sottoinsieme]] del [[Prodotto cartesiano|prodotto cartesiano]] tra l'insieme $A$ e quello $B$
$$R \subseteq A \times B$$

---

Se una [[Coppia|coppia]] di valori $(x, y) \in R$, allora possiamo scrivere $xRy$ e diciamo che *$x$ è $R$-correlato con $y$*

Una relazione si dice **binaria** quando il prodotto cartesiano viene fatto tra un insieme e se stesso

La **relazione inversa** di $R$ è la relazione $R^{-1} \subseteq B \times A$ dove:
$$R^{-1} = \{ (b, a)\ |\ (a, b) \in R \}$$

---

## Proprietà

### Riflessiva

Se $aRa\ \forall a \in A$

### Simmetrica

Se $aRb \Rightarrow bRa\ \forall a, b \in A$

### Transitiva

Se $aRb \land bRc \Rightarrow aRc\ \forall a, b, c \in A$

### Anti-simmetrica

Se $aRb \land bRa \Rightarrow a = b\ \forall a, b \in A$