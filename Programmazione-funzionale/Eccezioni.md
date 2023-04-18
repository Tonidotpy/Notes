---
 Created: 2022-06-17 13:53
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Eccezioni
Le **eccezioni** sono occorrenze di eventi che alterano il normale flusso di controllo di un programma.

Se un'**eccezione** non viene gestita nella procedura corrente:
- la procedura termina e l'**eccezione** viene sollevata di nuovo;
- se il *chiamante* non la gestisce l'**eccezione** viene sollevata nuovamente;
- se non trova alcun gestore di **eccezioni** viene utilizzato quello di *default*.

Le **eccezioni** possono essere implementate:
- in modo *semplice*:
	- all'inizio inserisco l'**eccezione** nello stack il *chiamante*;
	- quando l'**eccezione** viene sollevata:
		- rimuovo il *chiamante* e controlle se la gestisce;
		- se non la gestisce sollevo di nuovo l'**eccezione** e ripeto il procedimento;
- attraverso una *tabella degli indirizzi*.