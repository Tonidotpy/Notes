---
 Created: 2022-12-30 16:05
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [protocol]
---

Il **token passing** è un metodo di **accesso** al mezzo di trasmissione che viene utilizzato in alcune reti di comunicazione per **gestire** l'accesso al mezzo di trasmissione da parte di più dispositivi

---

Il diritto di **trasmissione** viene rappresentato dal possesso di un *token* che viene passato **sequenzialmente** da un nodo all'altro, il *token* non è altro che un **pacchetto**

Il problemi del token passing sono:
- L'*overhead* dovuto al token
- L'**elevata latenza**
- La presenza di un ***single point of failure*** (il token)