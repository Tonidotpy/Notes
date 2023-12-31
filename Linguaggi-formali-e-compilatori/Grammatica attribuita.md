---
Created: 2023-12-31 16:32
Author: Antonio Gelain
aliases:
  - Syntax-Directed Definitions
  - SDD
tags:
  - linguaggi-formali-e-compilatori
---

Una **grammatica attribuita** è un tipo di [[Grammatica|grammatica]] tale e quale a quella che siamo abituati ad utilizzare ad eccezione di due elementi aggiuntivi:
1. **Attributi**: che sono associati ai [[Simbolo|simboli]] della grammatica e possono essere: *numeri*, *tipi*, *riferimenti alla tabella dei simboli*, *ecc*...
2. **Regole**: che sono associate alle [[Produzione|produzioni]] della grammatica e di norma sono [[Funzione|funzioni]] degli attributi dei simboli della produzione

---

Gli **attributi** si suddividono in due categorie:
1. **Attributi sintetizzati**: sono gli attributi del *driver* di una produzione, questi sono definiti in funzione degli attributi dei simboli del *body* della produzione
2. **Attributi ereditati**: sono gli attributi dei non-terminali nel *body* della produzione e sono definiti in funzione degli altri simboli del *body* della produzione

Le grammatiche attribuite contenenti solo attributi sintetizzati vengono chiamate **S-attributed SDD**
Le grammatiche attribuite contenenti anche attributi ereditati vengono chiamate **L-attributed SDD** solamente se rispettano le seguenti condizioni:
- Per ogni prouzione $A \rightarrow X_{1} ... X_{n}$ la definizione di ogni $X_{j}.i$ utilizza solamente
    - Attributi ereditati di $A$
    - Attributi sintetizzati o ereditati dei fratelli sinistri di $X_{j}$ ovvero $X_{1} ... X_{j-1}$

---

La grammatica attribuita viene utilizzata per dare dei valori effettivi al [[Parse Tree|parse tree]] facendolo diventare un [[Parse tree annotato|parse tree annotato]]

Partendo dalle foglie dell'albero si applicano le regole associate alla produzione utilizzata, risalendo fino alla radice dell'albero ottenendo così il valore finale della parola
