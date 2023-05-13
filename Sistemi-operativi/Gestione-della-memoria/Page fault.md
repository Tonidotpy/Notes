---
 Created: 2023-05-12 15:45
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

Il **page fault** è un'[[Eccezioni|eccezione]] generata quando un [[Processo|processo]] cerca di accedere ad una [[Paginazione|pagina]] che non è presente in [[Memoria primaria|memoria]] e deve essere caricata

---

Nel caso in cui si verifichi un page fault il [[Sistema operativo|SO]] carica la pagina nella memoria centrale e modifica la [[Tabella delle pagine|tabella delle pagine]] settando il *valid* [[Bit|bit]] a `1`
Infine ripristina l'istruzione che ha causato il page fault

Nel caso in cui non sia presente alcuno spazio in memoria dove caricare le pagine, ne viene selezionata una da **scambiare**

Alcuni algoritmi per il rimpiazzamento delle pagine sono:
- L'[[Algoritmo FIFO|algoritmo FIFO]]
- L'[[Algoritmo Least-Recently-Used|algoritmo LRU]]
- Algoritmi basati sul **conteggio**:
	- L'[[Algoritmo Least-Frequently-Used|algoritmo LFU]]
	- L'[[Algoritmo Most-Frequently-Used|algoritmo MFU]]
- L'[[Algoritmo della seconda opportunità|algoritmo second chance]]