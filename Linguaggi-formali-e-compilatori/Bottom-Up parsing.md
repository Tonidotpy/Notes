---
 Created: 2023-12-29 13:00
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

**Bottom-up parsing** è una tecnica utilizzata dai [[Analisi sintattica|parser]] e consiste nella costruzione di una [[Derivazione|derivazione]] **rightmost**, perciò si procede dalle foglie verso la radice dell'[[Albero di derivazione|albero di derivazione]]

---

Il processo di bottom-up parsing è suddiviso in quattro parti:
1. All'inizio si parte con una [[Grammatica generativa|grammatica]] $\mathcal{G}$ e una parola $w$
2. Si costruisce un [[Automa a Stati Finiti|automa a stati finiti]] caratteristico per la grammatica
3. Si calcola la [[Tabella di parsing bottom-up]]
4. Infine, utilizzano la tabella, si lancia un [[Algoritmo|algoritmo]] chiamato [[Shift-Reduce|shift/reduce]] per effettuare il parsing vero e proprio della parola $w$ rispetto alla grammatica $\mathcal{G}$

Esistono diverse tipologie di parser bottom-up:
- [[Grammatica SLR(1)|SLR(1)]]
- [[Grammatica LR(0)|LR(0)]]
- [[Grammatica LR(1)|LR(1)]]
- [[Grammatica LALR(1)|LALR(1)]]

---

