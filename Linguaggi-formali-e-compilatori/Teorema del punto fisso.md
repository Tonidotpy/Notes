---
Created: 2023-10-06 13:25
Author: Antonio Gelain
aliases: 
tags:
  - linguaggi-formali-e-compilatori
---

Il **teorema del punto fisso** dice che, dato $S$ un [[Algoritmi-e-strutture-dati/Strutture dati/Insieme|insieme]] finito e $f: 2^{S} \rightarrow 2^{S}$ una [[Funzione monotona|funzione monotona]], allora $\exists m \in \mathbb{N}$ tale che esiste un'unica soluzione minima all'equazione $X = f(X)$, e questa soluzione è $f^{m}(\emptyset)$

---

## Dimostrazione

La dimostrazione si divide in due parti:
1. Innanzitutto bisogna dimostrare che $\exists m \in \mathbb{N}$ tale che $f^{m}(\emptyset)$ è soluzione per $X = f(X)$
   Per definizione stessa di $f(X)$ possiamo subito dire che $\emptyset \subseteq f(\emptyset)$, e poiché $f(X)$ è **monotona** allora possiamo anche dire che $\emptyset \subseteq f^{2}(\emptyset)$
   Quindi, per il [[Principio di induzione|principio di induzione]] possiamo affermare che $f^{i}(\emptyset) \subseteq f^{i+1}(\emptyset), \forall i \in \mathbb{N}$
   Dal momento che $2^{S}$ è finito si arriverà ad un certo punto in cui non si potranno più osservare cambiamenti a successive applicazioni di $f(X)$, perciò avremmo un indice $m$ tale che $f^{m}(\emptyset) = f^{m+1}(\emptyset) = f(f^{m}(\emptyset))$
   Si dice che siamo arrivati al *punto di saturazione* per cui possiamo dire che $f^{m}(\emptyset)$ è una soluzione per $X = f(X)$
2. Successivamente bisogna dimostrare che $f^{m}(\emptyset)$ è l'**unica soluzione minima**.
   Per assurdo supponiamo che esista un'altra soluzione $A$ per $X = f(X)$, quindi per ipotesi deve valere $A = f(A)$, e quindi anche $A = f(A) = f^{2}(A) = ... = f^{m}(A)$
   Supponiamo anche che $f^{m}(\emptyset) \subseteq f^{m}(A)$ poiché naturalmente l'[[Insieme vuoto|insieme vuoto]] è compreso in qualsiasi insieme ($\emptyset \subseteq A$) e la funzione $f$ è monotona
   Allora possiamo mettere assieme le due precedenti osservazioni e affermare che $f^{m}(\emptyset) \subseteq A$, per cui $f^{m}(\emptyset)$ è una soluzione **unica** ed è anche la **minima**