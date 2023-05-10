---
 Created: 2023-05-10 14:25
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

La **tabella delle pagine** è una tabella utilizzata per tenere traccia di quale [[Paginazione#^fa9895|frame]] corrisponde a quale [[Paginazione#^33fec8|pagina]] e per tradurre un [[Indirizzo logico|indirizzo logico]] da uno [[Indirizzo fisico|fisico]]

---

L'indirizzo generato dalla [[Central Process Unit|CPU]] viene diviso in due parti:
1. **Numero di pagine**: usato come indice nella tabella delle pagine
2. **Offset**: combinato con l'indirizzo base definisce l'indirizzo fisico

Una tabella delle pagine può essere implementata in due modi diversi:
1. **Implementazione tramite registri**: le righe della tabella vengono mantenute nei registri
2. **Implementazione in memoria**: la tabella risiede in memoria e vengono utilizzati due registri
	1. **Page-table base register** (*PTBR*): che contiene un riferimento alla tabella delle pagine
	2. **Page-table length register** (*PTLR*): che contiene la dimensione della tabella delle pagine ed è opzionale

La **protezione** viene realizzata associando un [[Bit|bit]] di protezione ad ogni frame