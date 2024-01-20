---
 Created: 2023-12-08 16:26
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

Il **teorema di Rayleigh** estende la formulazione di [[Teorema di Parseval|Parseval]] al caso dei [[Segnali non periodici|segnali aperiodici]] permettendone di calcolarne l'[[Energia di un segnale|energia]] a partire dal suo sviluppo utilizzando la [[Trasformata di Fourier|trasformata di Fourier]]
$$E_{x} = \int_{-\infty}^{+\infty} |x(t)|^{2} dt = \int_{-\infty}^{+\infty} |X(f)|^{2} df$$

---
>[!NOTE] $|X(f)|^{2}$ è detta **densità spettrale di energia**

Questo teorema non è applicabile se il segnale da cui è stata ricavata la trasformata è [[Segnale periodico|periodico]] in quanto, essendo il risultato un [[Treno di impulsi|treno di impulsi]], non è possibile elevare un impulso alla seconda (*il quadrato di un impulso non è definito!*)
