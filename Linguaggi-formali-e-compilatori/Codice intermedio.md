---
 Created: 2023-12-19 14:52
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Il **codice intermedio** è un [[Linguaggio|linguaggio]] di transizione utilizzato durante la [[Compilatore|compilazione]] per poter generare codice simile al [[Codice target|codice macchina]] ma indipendente dalla piattaforma

---

Il codice intermedio viene generato attraverso la traduzione di un [[Albero di derivazione|parse tree]]

Esistono principalmente tre tipi di rappresentazione del codice intermedio:
1. **Strutture a [[Grafo|grafo]]**: ricavate dai parse tree oppure direttamente dagli [[Abstract Syntax Tree|AST]]
2. **Codice a tre indirizzi**: permette di referenziare più di tre valori in un singolo statement (nella forma `x = y op z`), limitandone la complessità
3. **Codice in un altro linguaggio**: un vero e proprio [[Linguaggio di programmazione|linguaggio di programmazione]] diverso da quello di partenza, possibilmente più efficiente e/o semplice (esistono numerosi linguaggi che [[Compilatore|compilano]] in codice C, che a sua volta viene poi compilato in linguaggio macchina)
