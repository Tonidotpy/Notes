---
 Created: 2022-03-22 08:47
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Disposizioni

Dato un [[Analisi/Insiemi/Insieme|insieme]] $S = \{ a_1, a_2, ..., a_n \}$ di $n$ oggetti distinti il numero di allineamenti che si possono trovare con $r$ oggetti scelti tra gli $n$ oggetti ritenendo diversi due **allineamenti** o perché:
- contengono oggetti diversi;
- gli stessi oggetti appaiono in ordine diverso;
- ogni elemento compare **al più** una volta sola.

$$D_{n,k} = n \cdot (n-1) \cdot (...) \cdot (n - k + 1)$$
ossia
$$D_{n,k} = \frac{n!}{(n-k)!}$$

### Disposizioni con ripetizione
$$\#\Omega_r = n_1 \cdot n_2 \cdot ... \cdot n_r = \prod_{i=1} n_i^r\ \ \ \ \#S = r$$
Dato un [[Analisi/Insiemi/Insieme|insieme]] $S = \{ a_1, a_2, ..., a_n \}$ di $n$ oggetti distinti il numero di allineamenti che si possono trovare con $r$ oggetti scelti tra gli $n$ oggetti ritenendo diversi due **allineamenti** o perché:
- contengono oggetti diversi;
- gli stessi oggetti appaiono in ordine diverso;
- uno stesso oggetto si ripete un numero diverso di volte.
$$D_{n, k}^r = n^k$$

