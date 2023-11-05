---
Created: 2023-10-28 19:59
Author: Antonio Gelain
aliases:
  - Linguaggio delle asserzioni atomiche
tags:
  - logica-computazionale
---

Un **linguaggio asserzionale** (o *linguaggio delle asserzioni atomiche*) $\mathcal{L_{A}}$ è una [[Analisi/Insiemi/Insieme|insieme]] di [[Asserzione|asserzioni]] 
$$\mathcal{L_{A}} = \{ a \}$$

---
> [!INFO] Un linguaggio asserzionale, nella sua [[Rappresentazione estensiva|rappresentazione estensiva]], viene anche chiamato [[Alfabeto|alfabeto]]

La [[Rappresentazione intensiva|rappresentazione intensiva]] di un linguaggio asserzionale $\mathcal{L_{A}}^{i}$ è definita come:
$$\mathcal{L_{A}}^{i} = \langle \mathcal{E}, \{ \mathcal{C} \}, \{ \mathcal{P} \} \rangle$$
dove:
- $\mathcal{E} = \{ e \}$ è un [[Analisi/Insiemi/Insieme|insieme]] di [[Entità|entità]]
- $\{ \mathcal{C} \}$ è un insieme di **concetti**, dove il concetto è il nome di una **classe**
- $\{ \mathcal{P} \}$ è un insieme di **proprietà** dove la proprietà è il nome di una [[Relazione|relazione]]

Esistono tre tipi di linguaggi:
- **Linguaggi informali**: quei linguaggi definiti informalmente (e.g. linguaggi naturali e senza regole di produzione)
- **Linguaggi semi-formali**: quei linguaggi dove la sintassi è formalmente definita
- **Linguaggi formali** (o *linguaggi logici*): quei linguaggi dove anche la [[Funzione di interpretazione|funzione di interpretazione]] è definita formalmente