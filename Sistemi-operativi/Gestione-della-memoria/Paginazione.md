---
 Created: 2023-05-08 13:15
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

La **paginazione** è una tecnica che permette di risolvere il problema della [[Frammentazione esterna|frammentazione esterna]] della [[Memoria|memoria]]

---

La paginazione permette che lo [[Spazio di indirizzamento|spazio di indirizzamento]] fisico di un [[Processo|processo]] sia **non-contiguo**

La memoria fisica viene suddivisa in blocchi di **dimensione fissa** detti *frame* ^fa9895

La memoria logica viene divisa in blocchi della **stessa dimensione** detti *pagine* ^33fec8

Per tenere traccia di quali frame corrispondono a quali pagine si utilizza una [[Tabella delle pagine|tabella delle pagine]] ^7c364d