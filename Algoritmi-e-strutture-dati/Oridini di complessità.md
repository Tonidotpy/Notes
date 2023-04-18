---
 Created: 2022-12-10 22:07
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Gli **ordini di complessità** sono categorie utilizzate per descrivere la **velocità** di crescita di una funzione che rappresenta la complessità temporale di un algoritmo

---

Di seguito è riportata una tabella che mostra i **pricipali** ordini di complessità:

| $f(n)$     | Tipo         |
| ---------- | ------------ |
| $\log n$   | logaritmico  |
| $\sqrt n$  | sublineare   |
| $n$        | lineare      |
| $n \log n$ | loglineare   |
| $n^2$      | quadratico   |
| $n^3$      | cubico       |
| $2^n$      | esponenziale | 

## Notazioni

### $O$ grande

Sia $g(n)$ una **funzione di costo**
Indichiamo con $O(g(n))$ l'**insieme delle funzioni** $f(n)$ tali per cui:
$$\exists c > 0, \exists m \ge 0\ |\ f(n) \le cg(n), \forall n \ge m$$
Perciò $f(n) = O(g(n))$ e $g(n)$ è un **limite asintotico superiore** per $f(n)$

### $\Omega$ grande

Sia $g(n)$ una **funzione di costo**
Indichiamo con $\Omega(g(n))$ l'**insieme delle funzioni** $f(n)$ tali per cui:
$$\exists c > 0, \exists m \ge 0\ |\ f(n) \ge cg(n), \forall n \ge m$$
Perciò $f(n) = \Omega(g(n))$ e $g(n)$ è un **limite asintotico inferiore** per $f(n)$

### $\Theta$ grande

Sia $g(n)$ una **funzione di costo**
Indichiamo con $\Theta(g(n))$ l'**insieme delle funzioni** $f(n)$ tali per cui:
$$\exists c_{1} > 0, \exists c_{2} > 0, \exists m \ge 0\ |\ c_{1}g(n) \le f(n) \le c_{2}g(n), \forall n \ge m$$
Perciò $f(n) = \Theta(g(n))$ e $g(n)$ è **cresce esattamente** come $f(n)$

### $o$ piccolo

Sia $g(n)$ una **funzione di costo**
$$\lim_{n \to \infty} \frac{f(n)}{g(n)} = 0 \Rightarrow f(n) = o(g(n))$$

### $\omega$ piccolo

Sia $g(n)$ una **funzione di costo**
$$\lim_{n \to \infty} \frac{f(n)}{g(n)} = +\infty \Rightarrow f(n) = \omega(g(n))$$

---

## Proprietà

### Dualità
$$f(n) = O(g(n)) \iff g(n) = \Omega(f(n))$$
### Eliminazione delle costanti
$$f(n) = O(g(n)) \iff af(n) = O(g(n)), \forall a > 0$$
$$f(n) = \Omega(g(n)) \iff af(n) = \Omega(g(n)), \forall a > 0$$
### Sommatoria
$$f_{1}(n) = O(g_{1}(n)), f_{2}(n) = O(g_{2}(n)) \Rightarrow f_{1}(n) + f_{2}(n) = O(\max(g_{1}(n), g_{2}(n)))$$
$$f_{1}(n) = \Omega(g_{1}(n)), f_{2}(n) = \Omega(g_{2}(n)) \Rightarrow f_{1}(n) + f_{2}(n) = \Omega(\max(g_{1}(n), g_{2}(n)))$$
### Prodotto
$$f_{1}(n) = O(g_{1}(n)), f_{2}(n) = O(g_{2}(n)) \Rightarrow f_{1}(n) \cdot f_{2}(n) = O(g_{1}(n) \cdot g_{2}(n)))$$
$$f_{1}(n) = \Omega(g_{1}(n)), f_{2}(n) = \Omega(g_{2}(n)) \Rightarrow f_{1}(n) \cdot f_{2}(n) = \Omega(g_{1}(n) \cdot g_{2}(n)))$$
### Simmetria
$$f(n) = \Theta(g(n)) \iff g(n) = \Theta(f(n))$$
### Transitività
$$f(n) = O(g(n)), g(n) = O(h(n)) \Rightarrow f(n) = O(h(n))$$

## Caratteristiche

Le **funzioni polinomiali** hanno complessità:
$$f(n) = a_{k}n^{k} + a_{k-1}n^{k-1} + ... + a_{1}n + a_{0}, a_{k} > 0 \Rightarrow f(n) = \Theta(n^{k})$$