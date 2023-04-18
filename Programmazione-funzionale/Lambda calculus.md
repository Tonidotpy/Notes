---
 Created: 2022-06-18 15:38
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Lambda calculus
Le **espressioni** del $\lambda$-calculus sono:
- *nome* ($n$), funzione o applicazione di un espressione ($e$) ad un espressione;
- *funzione:* $\lambda n.e$;
- *applicazione*: $e_{1}\ e_{2}$.

Un **espressione** $e$ può essere:
- un **identificatore** x (variabile o costante);
- una **funzione** $\lambda x.e$;
- un'**applicazione** $e\ e$.

Una **variabile** $x$ presente in un'**espressione** $e$ si dice **vincolata**, dunque se rimpiaziamo $\lambda x$ con $\lambda y$ e ogni occorrenza di $x$ in $e$ con $y$ la semantica non cambia.

In un'**espressione** $e$ denotiamo con $F_{v}(e)$ le **variabili libere** e $B_{v}(e)$ quelle **vincolate**.
Se $F_{v}(x) = \{ x \}$ e $B_{v}(x) = \emptyset$ allora:
- $F_{v}(e_{1}\ e_{2}) = F_{v}(e_{1}) \cup F_{v}(e_{2})$;
- $B_{v}(e_{1}\ e_{2}) = B_{v}(e_{1}) \cup B_{v}(e_{2})$.

Una **funzione** rimuove la variabile dalla lista delle variabili libere e l'aggiunge a quella di quelle vincolate:
- $F_{v}(\lambda x.e) = F_{v}(e) - \{ x \}$;
- $B_{v}(\lambda x.e) = B_{v}(e) \cup \{ x \}$.

In un'**espressione** $e$ si può rimpiazzare ogni occorrenza di $x$ con $e'$, $e[e'/x]$:
- se $x$ è un **identificatore**, $x[e'/x] = e'$;
- se $x \ne y$ è un **identificatore**, $y[e'/x] = y$;
- $(e_{1}\ e_{2})[e'/x] = (e_{1}[e'/x]\ e_{2}[e'/x])$;
- se $x \ne y$ e $y \notin F_{v}(e')$ allora $(\lambda y.e)[e'/x] = (\lambda y.e[e'/x])$;
- se $x = y$ allora $(\lambda y.e)[z/x] = (\lambda y.e)$.

Due **espressioni** sono **$\alpha$-equivalenti** se una può essere ottenuta dall'altra sostituendo solo le variabili vincolate.

La **$\beta$-equivalenza** è definita come $(\lambda x.e)e' \to_{\beta} e[e'/x]$ dove $(\lambda x.e)e'$ viene chiamato **redex** (o *espressione riducibile*) che viene ridotta in $e[e'/x]$.
In una **$\beta$-equivalenza** $e_{1} =_{\beta} e_{2}$:
- deve esserci una sequenza di **$\beta$-riduzioni** da $e_{1}$ a $e_2$;
- deve esistere una relazione $e_{1} \to_{\beta} e_{2}$ tale che sia **riflessiva** e **transitiva**. 

Le **$\beta$-riduzioni**:
- **non** sono **simmetriche**: $e_{1} \to_{\beta} e_{2} \ne e_{2} \to_{\beta} e_{1}$;
- non si possono eseguire se l'**espressione** non ha **redex**;
- possono anche non terminare in una **forma normale** (non ulteriormente riducibile).