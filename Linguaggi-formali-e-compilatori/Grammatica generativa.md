---
Created: 2023-09-12 09:49
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---
Una **grammatica generativa** è un tipo di grammatica utilizzata per generare [[Linguaggi-formali-e-compilatori/Linguaggio|linguaggi]]

---

Una grammatica è definita da:
 1. Un [[Vocabolario|vocabolario]]
 2. Un [[Analisi/Insiemi/Insieme|set]] di [[Simbolo|simboli]]
 3. Un insieme di [[Produzione|produzioni]] (o *regole*)

Formalmente una grammatica viene definita come una [[Tupla|tupla]] $\mathcal{G} = (V, T, S, P)$:
- $V$ è il **vocabolario** (simboli terminali e non, completo)
- $T$ è il set di simboli terminali
- $S$ è lo *start symbol*
- $P$ è il set delle produzioni

Una grammatica si dice **ambigua** se esiste $\omega \in \mathcal{L}(\mathcal{G})$ che può essere derivata da due [[Derivazione|derivazioni canoniche]] distinte, entrambe *rightmost* oppure *leftmost*

---

## Notazioni

Si utilizzano:
- Lettere maiuscole all'inizio dell'alfabeto ($A, B, ...$) per definire un simbolo non terminale
- Lettere maiuscole alla fune dell'alfabeto ($..., Y, Z$) per definire simboli appartenenti al vocabolario
- Lettere minuscole all'inizio dell'alfabeto ($a, b, ...$) per indicare caratteri terminali
- Lettere minuscole greche all'inizio dell'alfabeto ($\alpha, \beta, ...$) per indicare possibili stringhe formate dai simboli del vocabolario
- Lettere minuscole greche alla fine dell'alfabeto con pedice numerico ($\omega, \omega_{0}, ...$) per indicare stringhe di caratteri terminali
