---
 Created: 2022-03-08 12:46
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Algebra

> Consideriamo uno [[Spazio campionario|spazio campionario]] $\Omega$.
> Una chiave $A$ di parti di $\Omega$ si dice **algebra**) se:
> 1. $\Omega \in A$;
> 2. Se $a \in A$ allora $a^C \in A$;
> 3. Se $\{ a_i \}_{i=1}^n\ |\ a_i \in A$, allora $\bigcup_{i=1}^n a_i \in A$.

--- 

##### Teorema
Date due **algebre** $A_1$ e $A_2$ di $\Omega$ alora $A_1 \cap A_2$ è un'algebra di $\Omega$.

##### Dimostrazione
1. $\Omega \in A_1$, $\Omega \in A_2$ allora $\Omega \in A_1 \cap A_2$;
2. $a \in A_1$, $a \in A_2$ allora $a^C \in A_1$, $a^C \in A_2$ quindi $a^C \in A_1 \cap A_2$;
3. $a, b \in A_1$, $a, b \in A_2$ allora $a \cup b \in A_1$, $a \cup b \in A_2$ quindi $a \cup b \in A_1 \cap A_2$.