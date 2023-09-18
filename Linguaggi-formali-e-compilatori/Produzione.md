---
Created: 2023-09-12 10:06
Author: Antonio Gelain
aliases:
  - Regola
tags:
---

Una **produzione** ($\rightarrow$) è una regola di scrittura che permette di mappare una stringa ad un'altra rispettando la seguente limitazione:
- La stringa di partenza deve contenere almeno un [[Simbolo|simbolo]] **non terminale**

Esempio: $\{ S \rightarrow aSb,\ S \rightarrow ab \}$

La definizione formale dell'oggetto produzione si traduce in:
$$\delta \rightarrow \beta$$
Dove $\delta \in V^{+}$, ossia $\delta$ contiene almeno un simbolo non terminale e non è vuota ($\epsilon$)

>[!INFO] $\delta$ è detto **driver** della produzione mentre $\beta$ è detto **body** della produzione