---
Created: 2023-10-28 22:28
Author: Antonio Gelain
aliases: 
tags:
  - logica-computazionale
---

Un **modello mondiale** viene definito dalla seguente tripla formata da un [[Linguaggio asserzionale|linguaggio asserzionale]], un [[Dominio di interpretazione|dominio]] ed una [[Funzione di interpretazione|funzione di interpretazione]] 
$$\hat{\mathcal{W}} = \langle \mathcal{L_{A}}, D, \mathcal{I_{A}} \rangle$$

---

Il modo più comune per costruire un modello mondiale è quello di definire un [[Analisi/Insiemi/Insieme|insieme]] di [[Asserzione|asserzioni]], ossia quello che chiamiamo [[Teoria|teoria]]

In un modello mondiale abbiamo due possibili situazioni:
1. **Correttezza**: verificata se $\forall a \in \mathcal{T_{A}}\ |\ \mathcal{I_{A}}(a) = f \in M$
2. **Completezza**: verificata se $\forall f \in M, \exists a \in \mathcal{T_{A}}\ |\ \mathcal{I_{A}}(a) = f$

Il processo utilizzato per risolvere problemi utilizzando un modello del mondo è il seguente:
- **Inviare** *dati e conoscenza* dal gestore del sistema al sistema stesso, questo richiede la specifica di un linguaggio $\mathcal{L_{T}}$
- **Porre** una *domanda* da un utente al sistema, questo richiede la specifica di un linguaggio $\mathcal{L_{Q}}$
- **Rispondere** ad una *domanda* posta dall'utente, questo richiede la specifica di un linguaggio $\mathcal{L_{A}}$

> [!INFO] Solitamente i linguaggi $\mathcal{L_{Q}}$ e $\mathcal{L_{A}}$ combaciano

---

La [[Rappresentazione intensiva|rappresentazione intensiva]] di un modello mondiale, chiamata anche **stampo del modello mondiale**, è definita come:
$$\hat{\mathcal{W}}^{i} = \langle \mathcal{L_{A}}^{i}, D^{i}, \mathcal{I_{A}}^{i} \rangle$$

---

Data una [[Teoria asserzionale|teoria]] $\mathcal{T}$ ed un modello $M$ di $\mathcal{\hat W}$, possiamo dire che:
$$\begin{matrix}
M \vDash_{\mathcal{L_{A}}} a \\
M \vDash_{\mathcal{L_{A}}} \mathcal{T}
\end{matrix}$$
ossia che $M$ [[Relazione di implicazione|implica semanticamente]] $a$ e $\mathcal{T}$