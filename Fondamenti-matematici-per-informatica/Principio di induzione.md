---
 Created: 2022-03-08 17:06
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Principio di induzione

> SIa $\{ P(n) \}_{ n \in \mathbb{N} }$ una  famiglia di proposizioni (ovvero *affermazioni*) indicizzata su $\mathbb{N}$, allora supponiamo che:
> 1. $P(0)$ è vera (**base dell'induzione**);
> 2. $\forall n \in \mathbb{N}$, ($P(n) \Rightarrow P(succ(n))$) (**passo induttivo**).

---

##### Assiomi di Peano
1. $0 \in \mathbb{N}$ - esistenza di un elemento $0$;
2. $\exists$ una funzione successivo: $\mathbb{N} \mapsto \mathbb{N}$ è [[Iniettività|iniettiva]];
3. $succ(\mathbb{N}) \subseteq \mathbb{N} \backslash \{ 0 \}$ ovvero $\forall n \in \mathbb{N}, succ(n) \neq 0$;
4. Sia $A$ un [[Sottoinsieme|sottoinsieme]] di $\mathbb{N}$.
  Supponiamo che:
	1. $0 \in A$ (**base dell'induzione**)
	2. $\forall n \in \mathbb{N}$ ($n \in A \Rightarrow succ(n) \in A$) ovvero se $n \in A$ allora anche $succ(n) \in A$, allora $A = N$ (**passo induttivo**).

Sia $m \in \mathbb{N} \backslash \{ 0 \}$.
Allora $\exists ! n \in \mathbb{N}\ |\ succ(n) = m$.

###### Dimostrazione
Se $n$ esiste allora è unico, infatti se $n \in \mathbb{N}$ avesse la stessa proposizione allora $succ(n) = m = succ(n')$.

###### Corollario
$\mathbb{N}\ e\ \mathbb{N} \backslash \{ 0 \}$ sono [[Insiemi equipotenti|equipotenti]].
