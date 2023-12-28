---
 Created: 2023-12-28 17:19
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **grammatica con ricorsione sinistra** è un tipo di [[Grammatica libera|grammatica]] per cui, per qualche $A$ e $\alpha$, $A \Rightarrow^{*} A \alpha$

---

Se all'interno della grammatica è presente una [[Produzione|produzione]] nella seguente forma $A \rightarrow A \alpha$, questa viene detta ***ricorsione sinistra immediata**

> [!IMPORTANT] Se una grammatica $\mathcal{G}$ presenta ricorsione sinistra, allora tal grammatica **NON** appartiene alla classe [[Grammatica LL(1)|LL(1)]]

## Eliminazione della ricorsione sinistra immediata

Per eliminare la ricorsione sinistra immediata da una grammatica bisogna considerarne la sua forma:
$$A \rightarrow A \alpha_{1}\ |\ ...\ |\ A \alpha_{n}\ |\ \beta_{1}\ |\ ...\ |\ \beta_{k}$$
dove $\alpha_{j} \ne \epsilon\ \ \forall j : 1 \le j \le n$ e anche $\beta_{i} \ne A \gamma_{i}\ \ \forall i : 1 \le i \le k$
Questa verrà poi sostituita con la seguente forma:
$$
\begin{matrix}
A \rightarrow \beta_{1} A'\ |\ ...\ |\ \beta_{k} A' \\
A' \rightarrow \alpha_{1} A'\ |\ ...\ |\ a_{n} A'\ |\ \epsilon
\end{matrix}
$$
dove $A'$ è un nuovo terminale creato che non è già presente nella grammatica

## Eliminazione della ricorsione sinistra

L'eliminazione della ricorsione sinistra non è possibile per tutte le grammatiche, in ogni caso, l'idea è di ridurre gli steps della [[Derivazione|derivazione]] $A \Rightarrow^{*} A \alpha$, in modo da ottenere una produzione che presenta ricorsione sinistra immediata e successivamente applicare l'eliminazione della ricorsione sinistra immediata

> [!IMPORTANT] La procedura di eliminazione della ricorsione sinistra non sempre garantisce di ottenere grammatiche LL(1)
