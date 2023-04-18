---
 Created: 2022-06-18 13:35
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Programmazione logica
Siano una **collezione di assiomi** i cui teoremi sono stati provati.
Il programmatore **dichiara un teorema** (o *goal*) e il linguaggio tenta di trovare una **collezione di assiomi** che implicano quel teorema.

In molti linguaggi tali **assiomi** vengono scritti in una forma standard conosciuta come **horn clause**.
Una **horn clause** consiste in una *testa* $H$ e un *corpo* $B$ e si scrive:
$$H \Leftarrow B_{1}, B_{2}, ..., B_{n}$$
Se ogni $B_{i}$ è vero allora vuol dire che anche $H$ è vera.

Si possono estendere le [[Regola|dichiarazioni]] attraverso un processo chiamato **risoluzione**:
- se $A$ e $B$ implicano $C$ e $C$ implica $D$ allora si può dedurre che anche $A$ e $B$ implicano $D$.
$$C \Leftarrow A, B;\ \ \ D \Leftarrow C;\ \ \ D \Leftarrow A,B$$
Si può semplificare una [[Regola|regola]] fissando dei parametri, questo processo di associazione di variabili viene chiamato **unificazione**:
- $A(a, 2)$;
- $A(a, 3)$;
- $A(b, 1)$;
- $A(b, 3)$;
- $B(X, Y) \Leftarrow A(X, Z), A(Y, Z)$
- fissando $X$ ad $a$ e $Z$ a $3$ otteniamo:
$$B(a, Y) \Leftarrow A(Y, 3)$$

Variabili con un **valore fissato** come risultato di un'**unificazione** vengono dette **istanziate**.