---
 Created: 2023-12-09 13:49
 Author: Antonio Gelain
 Aliases: []
 Tags: [fondamenti-di-elaborazione-dei-segnali]
---

La **risposta in frequenza** di un [[Sistema lineare tempo-invariante|sistema LTI]] è la [[Trasformata di Fourier|trasformata di Fourier]] della risposta impulsiva, oppure il rapporto tra gli [[Spettro di un segnale|spettri]] dei segnali in ingresso ed in uscita
$$y(t) = x(t) * h(t) \rightarrow Y(f) = X(f) \cdot H(f) \Rightarrow H(f) = \frac{Y(f)}{X(f)}$$

---

A partire dalla risposta in frequenza si possono ricavare 3 funzioni
- [[Risposta in ampiezza]]
- [[Risposta in fase]]
- [[Ritardo di gruppo]]

## Composizione di funzioni di trasferimento

### Serie

Collegando in cascata due o più sistemi $H_{i}(f)$ possiamo ottenere la risposta in frequenza del sistema totale tramite il [[Moltiplicazione|prodotto]] delle risposte in frequenza dei singoli sistemi
$$Y(f) = X(f) \cdot \prod_{i=0}^{n} H_{i}(f) \Rightarrow H(f) = \frac{Y(f)}{X(f)} = \prod_{i=0}^{n} H_{i}(f)$$

### Parallelo

Collegando in parallelo due o più sistemi $H_{i}(f)$ possiamo ottenere la risposta in frequenza del sistema totale tramite la [[Addizione|somma algebrica]] delle risposte in frequenza dei singoli sistemi
$$Y(f) = X(f) \cdot \sum\limits_{i=0}^{n} H_{i}(f) \Rightarrow H(f) = \frac{Y(f)}{X(f)} = \sum\limits_{i=0}^{n} H_{i}(f)$$

### Retroazione negativa

In un sistema di retroazione, dove l'uscita di un sistema viene riportata in ingresso al sistema stesso (passandone per un altro), la risposta in frequenza del sistema totale è pari a:
$$Y(f)[1 + H_{1}(f) \cdot H_{2}(f)] = X(f) \cdot H_{1}(f) \Rightarrow H(f) = \frac{H_{1}(f)}{1 + H_{1}(f) \cdot H_{2}(f)}$$