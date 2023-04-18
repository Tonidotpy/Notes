---
 Created: 2022-03-11 12:49
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Funzioni
>Sia $f$ una [[Relazioni|relazione]] tra $X$ e $Y$, cioè $f \subset X \times Y$.
>$f$ si dice **funzione di $X$ e $Y$** (*applicazione mappa*) se:
> $$\forall x \in X, \exists ! \ y \in Y\ |\ xfy \iff (x, y) \in f$$

In questo caso scriviamo $f: X \mapsto Y$ e si dice che $X$ è il [[Dominio|dominio]] di $f$, $y$ è il [[Codominio|codominio]] di $f$.

###### Osservazione
Una **funzione** è una *tupla* $(X, Y, f)$ dove $X$ e $Y$ sono due [[Insiemi|insiemi]], $f$ è una [[Relazioni|relazione]] tra $X$ e $Y$ (cioè $f \subset X \times Y$)

---

##### Funzione come legge
Siano $X$ e $Y$ due [[Insiemi|insiemi]] non vuoti.
Una funzione $f: X \mapsto Y$ (come legge visto il concetto primitivo) è una legge che ad ogni $x \in X$ associa un **unico** $y \in Y$.

> Dati $X$ e $Y$ due [[Insiemi|insiemi]] (eventualmente vuoti) definiamo l'insieme $Y^X$ l'[[Insiemi|insieme]] contenente la funzione del tipo $f: X \mapsto Y$

###### Composizione
Siano $X, Y, Z$ tre [[Insiemi|insiemi]] non vuoti e $f: X \mapsto Y$ e $g: Y \mapsto Z$ due funzioni.
Definiamo la **composizione** $g \circ f: X \mapsto Z$ detta composizione di $f$ e $g$.

###### Immagine e controimmagine
Siano $X$ e $Y$ due [[Insiemi|insiemi]] non vuoti e sia $f: X \mapsto Y$.
Dato $A \subset X$, definiamo l'**immagine** di $A$ **tramite** $f$ come segue:
$$f(A) := \{ y \in Y\ |\ \exists x \in A\ |\ y = f(x) \}$$

$f(x)$ si dice **immagine** di $f$.
*Def*: Dato $B \subset Y$, definiamo la **controimmagine** di $B$ **tramite** $f$ ponendo:
$$f^{-1}(x) := \{ x \in X\ |\ f(x) \in B \}$$

Se $B = \{ y \}$ allora si dice **fibra di $f$  sopra $y$**:
$$f^{-1}(y) = f^{-1}(\{ y \}) = \{ x \in X\ |\ f(x) = y \}$$

###### Iniettività e suriettività
- $f$ è **iniettiva** se $\forall x_1, x_2 \in X\ |\ x_1 \neq x_2$ oppure se le fibre sono vuote o singoletti;
- $f$ è **suriettiva** (o *surgettiva*) se $f(x) = y$ ossia $\forall y \in Y, \exists x \in X\ |\ f(x) = y$ oppure se le fibre sono singoletti;
- $f$ è **biettiva** (o *bigettiva*) se è sia iniettiva che suriettiva.

