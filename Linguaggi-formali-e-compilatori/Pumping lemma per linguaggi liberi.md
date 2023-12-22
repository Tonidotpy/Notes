---
Created: 2023-09-22 09:13
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---

Il **pumping lemma** riguarda la presenza in ogni [[Grammatica libera|linguaggio libero]] infinito di [[Successioni|successioni]] di stringhe che presentano regolarità ben definite.

---

>[!INFO] Il pumping lemma viene utilizzato per dimostrare che un linguaggio **NON** è libero

Consideriamo un linguaggio libero $\mathcal{L}$, allora:
- $\exists p \in \mathbb{N}^{+}$ tale che
- $\forall z \in \mathcal{L}\ :\ |z| > p$, allora
- $\exists u, v, w, x, y$ tale che:
    - $z = uvwxy \land$
    - $|vwx| \le p \land$
    - $|vx| > 0 \land$
    - $\forall i \in \mathbb{N}.uv^{i}wx^{i}y \in \mathcal{L}$

## Dimostrazione

Consideriamo un linguaggio libero $\mathcal{L}$ che non comprende la **parola vuota** ($\epsilon \notin \mathcal{L}$)
Osserviamo che per ogni possibile [[Albero di derivazione|albero di derivazione]], ogni cammino dalla radice ad un terminale attraversa tanti non-terminali quanto il numero di archi attraversati

Definiamo $p$ come la lunghezza della **più lunga** parola derivabile tramite albero, e che inoltre sia tale che i suoi cammini siano **al più** lunghi quanto il numero di non-terminali di $\mathcal{G}$
Consideriamo una parola $z \in \mathcal{L}$, più lunga di $p$ ($|z| > p$), possiamo quindi essere sicuri che esiste un albero di derivazione per $z$ che possiede **almeno** un cammino la cui lunghezza è strettamente maggiore del numero di non-terminali

Consideriamo, per qualche albero di derivazione, la più profonda coppia di occorrenze dello stesso non-terminale lungo un qualche cammino, ossia le ultime due occorrenze più distanti dalla radice

![[pumping-lemma-linguaggi-liberi-dimostrazione-1.png]]

Date le precedenti considerazioni possiamo suddividere la parola $z$ in cinque parti $u$, $v$, $w$, $x$ e $y$
Possiamo notare come è possibile generare un numero arbitrario di sottostringhe $v$, $x$ di $z$

![[pumping-lemma-linguaggi-liberi-dimostrazione-2.png]]

Allo stesso modo possiamo ottenere un sottoalbero di derivazioni $w$ a partire dal non-terminale meno in profondità

![[pumping-lemma-linguaggi-liberi-dimostrazione-3.png]]

La precedente dimostrazione vale solo per linguaggi che non contengono la parola vuota $\epsilon$, nel caso in cui non fosse così la dimostrazione vale comunque con una leggera accortezza

Considerato un linguaggio $\mathcal{L}$ che comprende $\epsilon$, possiamo ricavare una grammatica $\mathcal{G} = (V, T, S, \mathcal{P})$ che generi $\mathcal{L} \backslash \{ \epsilon \}$
A questo punto definiamo una nuova grammatica $\mathcal{G}'$, in cui andiamo semplicemente ad aggiungere un nuovo *start-symbol* insieme a due produzioni: una che punti verso lo *start-symbol* della grammatica precedente e una seconda che generi $\epsilon$
$$\mathcal{G}' = (V, T, S', \mathcal{P} \cup \{ S' \rightarrow S, S' \rightarrow \epsilon \})$$

---

Per dimostrare che un linguaggio non è libero utilizzando il *pumping lemma* per contraddizione bisogna seguire i seguenti step:
1. Si assuma che $\mathcal{L}$ è un linguaggio libero ^b0c485
2. $\mathcal{L}$ ha una **lunghezza di pumping** $P$
3. Tutte le stringhe più lunghe di $P$ possono essere *"pumped"*
4. Si trovi una stringa $z \in \mathcal{L}$ tale che $|z| \ge P$
5. Si divida $z$ in **5 parti** $uvwxy$
6. Si dimostri che $uv^{i}wx^{i}y \notin \mathcal{L}$ per qualche $i$
7. Si dimostri che la stessa cosa per tutte le possibili combinazioni di $uvwxy$ data la stessa $i$
8. $z$ non può essere *"pumped"* il che è una **contraddizione** col punto [[Pumping lemma per linguaggi liberi#^b0c485|[1]]]
