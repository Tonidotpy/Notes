---
 Created: 2022-12-17 19:49
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [HTTP,HTTP/1.0, HTTP/1.1, HTTP/1]
 Tags: [protocol]
---

**Hypertext Transfer Protocol** (*HTTP*) è un [[Protocollo|protocollo di rete]] utilizzato per scambiare **risorse**, come ad esempio pagine web, immagini e video, su [[Internet]]

---

Il protocollo HTTP utliizza il [[Transmission Control Protocol|TCP]] per garantire l'**integrità dei dati** trasmessi.

HTTP è un protocollo *stateless* ossia **senza stato** le informazioni sulle richieste **non** vengono **salvate** e devono essere ritrasmesse
Per ovviare a questo problema vengono utilizzati i [[Cookie]]

Le **connessioni** HTTP possono essere di **due** tipi:
1. **Connessioni persistenti**: possono essere trasmessi **più** oggetti su una singola connessione TCP
2. **Connessioni non persistenti**: almeno un oggetto viene trasmesso su una connessione TCP

HTTP utilizza la porta `80` per comunicare

---

## Richiesta HTTP

Un **messaggio** di richiesta HTTP in formato generale è composto da:
- una riga di **richiesta**
- più righe di **intestazione**
- un *carriage return* (\r) e un *line feed* (\n) extra che indicano la fine del messaggio
- Il **campo dell'entità**

![HTTP-request-message|350](https://www.studiotarantelli.it/img/esempio-protocollo-http.jpg)

Esistono diversi tipi di **metodi** per una richiesta HTTP:
- **GET**: invia le **informazioni** ricevute dall'utente concatenandole con l'**URL**
- **POST**: inserisce le **informazioni** ricevute dall'utente nel **campo** dell'entità
- **HEAD**: **esclude** l'oggetto richiesto dalla risposta
- **PUT** (HTTP/1.1): **include** il file nel corpo e lo **invia** al percorso specificato nel campo **URL**
- **DELETE** (HTTP/1.1): **cancella** il file specificato nel campo **URL**

---

## Risposta HTTP

Un messaggio di **risposta** HTTP è formato da:
- Una riga di **stato**
- Più righe di **intestazione**
- Una serie di **dati**

![HTTP-response-message|350](https://slideplayer.it/slide/1756585/7/images/29/Formato+generale+di+un+messaggio+di+risposta.jpg)

Lo **stato** di una risposta viene rappresentato attraverso *[[Protocollo|protocolo]]* + *codice* + *espressione* dove il codice è un numero a 3 cifre mentre l'espressione è una stringa che riassume il significato del codice

### Codici di stato

I **codici di stato** vengono categorizzati tramite il numero delle centinaia:
- **Codici 1xx** (*infomativi*): la richiesta è stata **ricevuta** e sta avvenendo la sua **elaborazione**
	- `100 Continue`
	- `101 Switching Protocols`
	- `102 Processing`
- **Codici 2xx** (*successo*): la richiesta è stata **ricevuta** ed e stata elaborata con **successo**
	- `200 OK`
	- `201 Created`
	- `202 Accepted`
- **Codici 3xx** (*reindirizzamento*): devono essere eseguite ulteriori **azioni** per soddisfare la richiesta
	- `300 Multiple Choices`
	- `301 Moved Permanently`
	- `302 Found`
- **Codici 4xx** (*errori lato client*): la richiestà **non** può essere **soddisfatta**
	- `400 Bad Request`
	- `401 Unauthorized`
	- `402 Payment Required`
	- `403 Forbidden`
	- `404 Not Found`
- **Codici 5xx** (*errori lato server*): il **server** ha fallito nel soddisfare la **richiesta**
	- `500 Internal Server Error`
	- `501 Not Implemented`
	- `502 Bad Gateway`

---
