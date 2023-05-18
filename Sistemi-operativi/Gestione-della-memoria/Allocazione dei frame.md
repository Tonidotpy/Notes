---
 Created: 2023-05-18 20:32
 Author: Antonio Gelain
 Aliases: []
 Tags: [gestione-della-memoria]
---

L'**allocazione dei frame** è il procedimento tramite cui i [[Paginazione#^fa9895|frame]] di un [[Processo|processo]] devono essere caricati in [[Memoria primaria|memoria]] per eseguirlo

---

Esistono due tipi di **allocazione**:
- [[Allocazione fissa]]
- [[Allocazione variabile]]
Esistono due tipi di **contesto** in cui vengono scelti i frame da sostituire in caso di [[Page fault|page fault]]:
- **Locale**: ogni processo seleziona solamente i frame che appartengono ad esso
- **Globale**: viene scelto un frame tra l'insieme di tutti i frame presenti in memoria indipendentemente dal processo

e due tipi di contesto dal quale vengono scelti i frame, illustrati nella seguente tabella:
| Allocazione\Contesto | Locale | Globale |
| ------------------- | ------ | ------- |
| Fissa               | Si     | No      |
| Dinamica            | Si     | Si      |

Esistono dei frame che **non possono** essere rimpiazzati (come ad esempio quelli corrispondenti a pagine del kernel)