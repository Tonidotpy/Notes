---
 Created: 2022-12-09 21:48
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **correttezza di un algoritmo** si riferisce alla sua capacità di **risolvere** il problema per cui è stato progettato in modo **accurato** e **preciso**
In altre parole, un algoritmo è considerato corretto se, quando viene eseguito, produce **sempre** risultati corretti e precisi per qualsiasi input **valido**

---

Per valutare la correttezza di un algoritmo si ricorre alle **invarianti** ossia delle **condizioni sempre vere** in un certo punto del programma
Le invarianti possono essere:
- **Invarianti di ciclo**: una condizione sempre vera all'**inizio** dell'iterazione di un **ciclo**
- **Invarianti di classe**: una condizione sempre vera al **termine** dell'esecuzione di un **metodo** della classe

Il concetto di invariante di ciclo ci aiuta a dimostrare la correttezza di un **algoritmo iterativo** tramite:
- **Inizializzazione** (*caso base*): la condizione è vera alla **prima iterazione** di un ciclo
- **Conservazione** (*passo induttivo*): se la condizione è vera **prima** di un'iterazione del ciclo allora rimane vera al **termine**
- **Conclusione**: quando il ciclo **termina** l'invariante deve rappresentare la *"correttezza"* dell'algoritmo