---
 Created: 2022-06-16 14:09
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Ambienti
Gli **ambienti** sono collezioni di associazioni tra [[Nomi|nomi]] e [[Oggetti denotabili|oggetti]] che esistono in un preciso tempo di esecuzione di un programma.

La **dichiarazione** è un meccanismo (implicto o esplicito) che crea un'**associazione** in un **ambiente**.

Un **ambiente** in un [[Blocchi|blocco]] specifico può essere diviso in:
- *ambiente locale*: associato all'ingresso di un [[Blocchi|blocco]];
- *ambiente non locale*: le associazioni vengono ereditate dagli altri [[Blocchi|blocchi]];
- *ambienti globali*: la parte dell'*ambiente non locale* che contiene associazioni comuni a tutti gli altri [[Blocchi|blocchi]].

###### Operazioni
In un **ambiente** si può:
- creare un associazione tra [[Nomi|nomi]] e [[Oggetti denotabili|oggetti]];
- fare riferimento ad un [[Oggetti denotabili|oggetto]] dato il suo [[Nomi|nome]];
- disattivare l'associazione tra [[Nomi|nome]] e [[Oggetti denotabili|oggetto]];
- riattivare l'associazione tra l'[[Oggetti denotabili|oggetto]] e il suo [[Nomi|nome]];
- rimuovere l'associazione tra [[Nomi|nome]] e [[Oggetti denotabili|oggetto]].

Un'**ambiente** è quindi definito da:
- regole di [[Visibilità|visibilità]];
- regole specifiche;
- regole sul passaggio dei parametri;
- regole sulle associazioni.