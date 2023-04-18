---
 Created: 2022-06-17 12:06
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Passaggio di parametri
Il **passaggio di parametri** avviene principalmente:
- per **valore**:
	- il valore viene copiato nel *parametro formale* della funzione che viene trattata come una variabile locale;
	- modificare il valore del *parametro formale* **non cambia** quello *attuale*;
	- se il parametro è passato per **risultato** allora al termine della funzione il valore del *parametro formale* viene copiato in quello attuale;
- per **riferimento**:
	- viene copiato il *riferimento* (indirizzo) del parametro attuale;
	- modificare il valore del *parametro formale* **cambia** anche quello *attuale*;
	- per risparmiare tempo e memoria il parametro può essere passato per *riferimento* ma **solo in lettura**.

Durante il passaggio di **funzioni come parametro** viene utilizzato l'[[Ambienti|ambiente non locale]]:
- al momento della creazione del link (*deep binding*);
- al momento della chiamata della funzione (*shallow binding*).