---
 Created: 2023-05-10 14:57
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

La **tabella dei segmenti** è una tabella che mappa gli [[Indirizzo logico|indirizzi logici]] formati dalla [[Coppia|coppia]] `{ numero di segmento, offset }` in [[Indirizzo fisico|indirizzi fisici]]

---

Ogni riga della tabella contiene:
- L'indirizzo fisico di partenza del [[Segmentazione|segmento]] in [[Memoria|memoria]]
- La lunghezza del segmento

Una tabella dei segmenti può essere implementata in memoria utilizzando due registri:
	1. **Segment-table base register** (*STBR*): che contiene un riferimento alla tabella dei segmenti
	2. **Segment-table length register** (*STLR*): che contiene la dimensione della tabella delle segmenti
