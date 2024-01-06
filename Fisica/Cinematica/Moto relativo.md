---
 Created: 2023-04-26 11:18
 Author: Antonio Gelain
 Aliases: []
 Tags: [cinematica]
---

Un **moto relativo** è un tipo di [[Movimento|moto]] che avviene in riferimento ad un [[Sistema di riferimento|sistema]] scelto (in generale anch'esso in movimento) 

---

Dato un **sistema di riferimento** $S$ che varia la sua posizione nel [[Tempo|tempo]] fino ad arrivare ad uno [[Stato|stato]] $S'$ sia $P$ un [[Punto|punto]] descritto dal vettore $\vec{r}$ in riferimento al sistema $S$

La posizione originale del punto è data dalla seguente formula:
$$\vec{r} = \vec{OO'} + \vec{r'}$$

[[Derivate|Derivando]] possiamo ottenere la [[Velocità|velocità]] relativa di quel punto:
$$\vec{v} = \frac{d\vec{OO'}}{dt} + \vec{v'} + \vec{\omega} \times \vec{r'}$$
Dove la [[Velocità di trascinamento|velocità di trascinamento]] è data da $\vec{v_{0}} = \frac{d\vec{OO'}}{dt} + \vec{\omega} \times \vec{r'}$

Derivando ulteriormente possiamo ottenere l'[[Accelerazione|accelerazione]] relativa al sistema del punto:
$$\vec{a} = \vec{a'} + \vec{a_{0}} + \frac{d\vec{\omega}}{dt} \times \vec{r'} + \vec{\omega} \times (\vec{\omega} \times {\vec{r'}}) + 2\vec{\omega} \times \vec{v'}$$
Dove l'[[Accelerazione di trascinamento|accelerazione di trascinamento]] è data da $\vec{a_{t}} = \vec{a_{0}} + \frac{d\vec{\omega}}{dt} \times \vec{r'} + \vec{\omega} \times (\vec{\omega} \times {\vec{r'}})$
e l'[[Accelerazione di Coriolì|accelerazione di Coriolì]] è data da $\vec{a_{c}} = 2 \vec{\omega} \times \vec{v'}$