---
 Created: 2023-12-29 16:36
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **tabella di parsing bottom-up** è un particolare tipo di [[Tabella di parsing|tabella]] che viene utilizzata dai [[Bottom-Up parsing|parser bottom-up]] per analizzare diversi tipi di [[Grammatica libera|grammatica]]

---

La tabella è composta nel seguente modo:
- Si hanno tante **righe** quanti gli stati dell'[[Automata|automa caratterstico]]
- Si ha una **colonna** per ogni [[Simbolo|simbolo]] nel [[Vocabolario|vocabolario]] $V \cup \{ \$ \}$
- Le celle vuote all'interno della tabella identificano casi di errore

La tabella dipende dall'automa caratteristico: automi diversi portano a tabelle diverse che portano a parsing diversi

