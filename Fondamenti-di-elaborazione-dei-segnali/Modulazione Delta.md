---
 Created: 2024-01-23 10:58
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **modulazione delta** è un metodo differenziale di [[Codifica|codifica]] dei [[Segnale|segnali]]

---

Anziché codificare i singoli valori dei campioni, vengono codificate le variazioni tra un campione e l'altro

Si definisce il passo $\Delta$, come la quantità fissa da aggiungere o sottrarre al campione corrente rispetto al precedente e basterà quindi associare 1 [[Bit|bit]] ad ogni campione per definirne univocamente il valore

La qualità del segnale ottenuto dalla modulazione delta sarà più bassa rispetto alla [[Modulazione a impulsi codificati|PCM]], e vengono introdotti un paio di errori:
1. Il primo errore avviene in presenza di variazioni brusche per cui la *funzione di inseguimento* non riesce a *inseguire* le variazioni del segnale (*slope overload*)
2. Il secondo tipo di errore avviene nelle zone piatte, in cui il segnale continua comunque ad oscillare tra $\mp \Delta$ (*quantization noise*)
