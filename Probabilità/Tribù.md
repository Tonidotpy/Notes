---
 Created: 2022-03-08 12:42
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Sigma algebra]
 Tags: []
---

# Tribù

> Considerato uno [[Spazio campionario|spazio campionario]] $\Omega$ una chiave $A$ di parti di $\Omega$ si dice **tribù** (o $\sigma$ *algebra*) se:
> 1. $\Omega \in A$;
> 2. Se $a \in A$ allora $a^C \in A$;
> 3. Se $\{ a_i \}_{i=1}^\infty\ |\ a_i \in A\ \forall i$, allora $\bigcup_{i=1}^\infty a_i \in A$.

---

- Considerata una *famiglia* $F$ di [[Sottoinsiemi|sottoinsiemi]] di $\Omega$ chiamiamo $A_F$ la **tribù generata** da $F$.
  $$A_F = \cap \{ A\ |\ A \text{ è una tribù e } F \subseteq A \}$$

##### Teorema
Date due **trbù** $A_1$ e $A_2$ di $\Omega$ alora $A_1 \cap A_2$ è un'tribù di $\Omega$.

##### Dimostrazione
1. $\Omega \in A_1$, $\Omega \in A_2$ allora $\Omega \in A_1 \cap A_2$;
2. $a \in A_1$, $a \in A_2$ allora $a^C \in A_1$, $a^C \in A_2$ quindi $a^C \in A_1 \cap A_2$;
3. $a, b \in A_1$, $a, b \in A_2$ allora $a \cup b \in A_1$, $a \cup b \in A_2$ quindi $a \cup b \in A_1 \cap A_2$.