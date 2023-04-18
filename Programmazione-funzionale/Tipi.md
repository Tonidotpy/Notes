---
 Created: 2022-06-17 14:47
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Tipi
Un **tipo** è una collezione di valori omogenei su cui possono essere eseguite operazioni.

I **tipi di dato** più utilizzati sono:

| Tipi         | Valori               | Rappresentazione          |
| ------------ | -------------------- | ------------------------- |
| *booleano*   | true, false          | 1 Byte                    |
| *carattere*  | 'a', '1', ...        | dipendente dalla codifica |
| *intero*     | 0,1, -1, ...         | 2-4 Byte                  |
| *reali*      | 0.1, -2.5, ...       | 8-16 Byte                 |
| *complessi*  | 1+2i, -2-7i, ...     | 2 interi                  |
| *void*       | a single value       | nessuna                   |
| enumerazioni | definiti dall'utente | 1 Byte per elemento       |
| intervalli   | (-10, 2), ...        |                           |

Esistono **tipi di dato strutturati** che sono strutture più complesse che utilizzano i **tipi di dato** di base:
| Tipi        | Info                                           |
| ----------- | ---------------------------------------------- |
| *record*    | collezione di campi anche eterogenei           |
| *array*     | collezione lineare di elementi omogenei        |
| *set*       | collezione di elementi unici senza ripetizioni |
| *puntatori* | riferimenti ad oggetti di un altro tipo        |

---
Due **tipi** $T$ ed $S$ sono **equivalenti** se ogni oggetto di tipo $T$ è anche un oggetto di tipo $S$ e viceversa.
Due **tipi** possono essere **equivalenti** se:
- hanno lo **stesso nome**;
- hanno la **stessa struttura**;

$T$ si dice **compatibile** se un qualsiasi oggetto di tipo $T$ può essere utilizzato in un contesto in cui uno di tipo $S$ è atteso.
Due **tipi** possono essere **compatibili** se:
- sono **equivalenti**;
- il valore di uno è un sottoinsieme dell'altro;
- tutte le operazioni sui valori di uno possono essere eseguite anche sull'altro;
- c'è una corrispondenza naturale tra i valori dei due **tipi**;
- i valori di uno possono essere fatti corrispondere a quelli dell'altro.

Se $T$ è **compatibile** con $S$ allora esiste un **meccanismo di conversione** che può essere:
- *conversione implicita* (o *coercizione*): la [[Macchine astratte|macchina astratta]] fa la conversione in automatico;
- *conversione esplicita* (o *cast*): la conversione è menzionata esplicitamente.

Se un valore può avere **tipi multipli** si dice che è **polimorfo**.
Esistono tre tipi di **polimorfismo**:
- *ad hoc*: lo **stesso simbolo** ha **diversi significati**;
- *universale*:
	- *parametrico*: quando il valore è associato ad un **numero infinito di possibili tipi**;
	- *di sottotipo*: quando il valore è associato ad un numero infinito di possibili **sottotipi** $S$ di un **tipo** $T$.