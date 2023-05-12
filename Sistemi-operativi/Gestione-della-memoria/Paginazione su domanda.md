---
 Created: 2023-05-12 15:39
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

La **paginazione su domanda** è un tipo di [[Paginazione|paginazione]] utilizzato per gestire la [[Memoria virtuale|memoria virtuale]] caricando in [[Memoria primaria|memoria]] solo le **pagine** necessarie per l'esecuzione dei [[Processo|processi]]

---

Per utilizzare questa tecnica è necessario conoscere lo [[Stato|stato]] delle pagine (in memoria o non), per questo viene salvato un [[Bit|bit]] (chiamato *valid* se a `1` oppure *invalid* se a `0`) per ogni riga della [[Tabella delle pagine|tabella delle pagine]]

Se durante la traduzione degli [[Indirizzo di memoria|indirizzi]] il bit associato è a `0` si ha una [[Page fault|page fault]]