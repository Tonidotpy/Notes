---
 Created: 2022-03-08 12:34
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [Popolazione di riferimento]
 Tags: []
---

# Spazio campionario

> Lo **spazio campionario** è la collezione di ==tutti== gli [[Esito|eventi elementari]] e viene indicato con $\Omega$.

---

- Gli elementi di $\Omega$ sono a due a due **incompatibili**, ossia può accaderne solamente uno alla volta;
- Sono **esaustivi**, ossia almeno uno degli elementi deve essere vero.

### Operazioni
- Dati due [[Analisi/Insiemi/Insieme|insiemi]] $A, B \subseteq \Omega$ si dicono **disgiunti** (o *incompatibili*) se $A \cap B = \emptyset$;
- Data una famiglia di [[Spazio probabilizzabile|spazi probabilizzabili]] $\{ \Omega_i, A_i \}_i \in I$ allora possiamo costruire uno [[Spazio probabilizzabile|spazio probabilizzabile]];
  $\Omega = \times_{i \in I} \Omega_i$ ottenuto come [[Prodotto cartesiano|prodotto cartesiano]] (**spazio campionario prodotto**)
  $A = \otimes_{i \in I} A_i$ [[Tribù]] prodotto
- Consideriamo $a_i \in A_i\ |\ a_i \ne \Omega_i$ al più per un numero finito e otteniamo $\prod_{i \in I} a_i$, questo è un "*rettangolo*" ($\Omega, A$) uno [[Spazio probabilizzabile|spazio probabilizzabile]];
- Supponiamo ora che ogni spazio ($\Omega_i, A_i P_{r_i}$) sia [[Spazio probabilizzato|probabilizzato]].

###### Regole di De Morgan
1. $(A \cup B)^C = A^C \cap B^C$ => $(\bigcap_{i = 1}^n A_i)^C = \bigcup_{i = 1}^n A_i^c$;
2. $(A \cap B)^C = A^C \cup B^C$ => $(\bigcup_{i = 1}^n A_i)^C = \bigcap_{i = 1}^n A_i^c$;
3. $(A^C)^C = A$.

Le regole di De Morgan valgono comunque anche per le **successioni numerabili** di [[Analisi/Insiemi/Insieme|insiemi]] $(A_i)_{i = 1}^\infty$.