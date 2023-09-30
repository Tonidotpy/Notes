---
 Created: 2023-09-29 09:07
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Una **grammatica regolare** è un particolare tipo di [[Grammatica libera|grammatica libera]] tale che le sue produzioni sono in una delle seguenti forme:
- Il *body* è un solo [[Simbolo|terminale]] ($A \mapsto a$)
- Il *body* è composto da un terminale e un non-terminale, nella seguente forma ($A \mapsto aB$)
- Il *body* è la parola vuota ($A \mapsto \epsilon$)

---

In genere i [[Linguaggio|linguaggi]] generati da queste grammatiche sono riconosciuti dagli [[Automa a Stati Finiti|automi a stati finiti]], sia deterministici che non deterministici

## Espressioni regolari

Un **espressione regolare** è un [[Insieme|insieme]] di tutti i simboli dell'alfabeto che abbiamo scelto e permette di **denotare** un linguaggio regolare

Se $r_{1}$ e $r_{2}$ sono espressioni regolari
- $r_{1}\ |\ r_{2}$ è un'espressione regolare, detta **alternanza**
- $r_{1} \cdot r_{2}$ è un'espressione regolare, scritta anche come $r_{1} r_{2}$ ed è detta **concatenazione**
- $r_{1}^{*}$ è un espressione regolare che significa **ripetizione** di $r$ per un certo numero di $k$ volte, detta ***Kleene star***
- $(r_{1})$ è un'espressione regolare, usata per definire l'ordine di svolgimento delle operazione ed è detta **parentesi**

>[!INFO] In assenza di parentesi l'ordine di precedenza delle operazioni precedentemente descritte è la seguente:
> $$\text{Kleene Star < Concatenazione < Alternanza}$$