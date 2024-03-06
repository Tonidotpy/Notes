---
Created: 2024-01-24 15:10
Author: Antonio Gelain
aliases:
  - DFT
tags:
  - fondamenti-di-elaborazione-dei-segnali
---

La **trasformata di Fourier discreta** è l'analogo nel dominio discreto della formula che restituisce i coefficienti della [[Serie di Fourier|serie di Fourier]]
$$X[k] = \frac{1}{\sqrt{N}} \sum\limits_{n = 0}^{N - 1} x[n] e^{-j2\pi \frac{k}{N} n} : k = 0, ..., N-1$$

---

L'**inversa** della trasformata di Fourier è l'analogo nel dominio discreto della serie di Fourier
$$x[n] = \frac{1}{\sqrt{N}} \sum\limits_{n = 0}^{N - 1} X[k] e^{j2\pi \frac{k}{N} n} : n = 0, ..., N-1$$

Le armoniche [[Campionamento|campionate]] $e^{-j2\pi \frac{k}{N} n}$ sono sinusoidi complesse discretizzate nel tempo e prendono il nome di **funzioni di base**

La DFT è una trasformata **ortogonale**, correlando due funzioni base $i, j$ con $i \ne j$ il risultato è `0`
