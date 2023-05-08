---
 Created: 2023-05-07 14:21
 Author: Antonio Gelain
 Aliases: [MMU]
 Tags: [gestione-della-memoria]
---

La **memory management unit** (o *MMU*) è un dispositivo [[Hardware|hardware]] che mappa [[Indirizzo logico|indirizzi virtuali]] in [[Indirizzo fisico|indirizzi fisici]]

---

L'MMU consiste di [[Registro di rilocazione|registri di rilocazione]] che permettono di proteggere lo [[Spazio di indirizzamento|spazio di indirizzamento]] dei vari [[Processo|processi]]

Tali registri contengono:
- Il valore dell'**indirizzo minore** ([[Registro di base|registro di base]])
- Il **limite superiore** dello spazio logico ([[Registro limite|registro limite]])