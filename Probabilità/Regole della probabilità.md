---
 Created: 2022-03-09 13:36
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Regole della probabilità
1. Se $A$ è un [[Esito|evento]] con $P_r(A)$ allora la  $P_r(A^C) = 1 - P_r(A)$;
   $\Omega = A \cup A^C\ \emptyset = A \cap A^C$
   abbiamo che $P_r(\Omega) = P_r(A \cup A^C) = P_r(A) + P_r(A^C)$
   abbiamo che $P_r(\Omega) = 1$
   quindi $1 = P_r(A) + P_r(A^C) \iff P_r(A^C) = 1 - P_r(A)$.
   *Nota*: $\emptyset = \Omega^C$ allora $P_r(\emptyset) ? 1 - P_r(\Omega) = 0$.
2. Se $A$ e $B$ sono due [[Esito|eventi]] allora $P_r(A \cup B) = P_r(A) + P_r(B) - P_r(A \cap B)$;
   $A \cup B = A \cup(B \cap A^C)$           $A \cap(B \cap A^C) = \emptyset$
   $B = (A \cap B) \cup (B \cap A^C)$          $(A \cap B) \cap (B \cap A^C) = \emptyset$
   $P_r(A \cup B) = P_r(A) + P_r(B \cap A^C)$
   $P_r(B) = P_r(A \cap B) + P_r(B \cap A^C)$
   $P_r(A \cup B) - P_r(B) = P_r(A) - P_r(A \cap B)$.
3. Se $A \subseteq B$ allora $P_r(A) \le P_r(B)$;
   $B = (A \cap B) \cup (B \cap A^C) = A \cup (B \cap A^C)$
   $P_r(B) = P_r(A) + P_r(B \cap A^C) \ge P_r(A)$.
   *Nota*: La regola 3 implica che $P_r(A) \le 1 = P_r(\Omega)$ per ogni [[Esito|evento]] di $A$ per ogni $A \subseteq \Omega$.
   *Nota*: Se due [[Esito|eventi]] $A$ e $B$ sono equivalenti $A \subseteq B$ e $B \subseteq A$ allora $P_r(A) = P_r(B)$.
4. **Disuguaglianza di Bonferroni**: Se $A_1, A_2, ..., A_n$ sono $n$ [[Esito|eventi]] allora:
   $$\sum_{i=1}^n P_r(A_i) - \sum_{1 \le i < j \le n} P_r(A_i \cap A_j) = P_r(\bigcup_i A_i) \le \sum_i P_r(A)$$