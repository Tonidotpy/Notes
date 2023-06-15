---
 Created: 2023-04-14 15:11
 Author: Antonio Gelain
 Aliases: []
 Tags: [file-system]
---

Un **file** è un contenitore, o fascicolo di **informazioni/[[Dato|dati]]** in formato digitale identificato da un nome

---

Vengono memorizzate in [[Memoria secondaria|memoria]] nella struttura della directory:
- **Nome**
- **Tipo**: la tipologia del file (audio, video, immagine, testo, ...)
- **Posizione**: l'[[Indirizzo fisico|indirizzo fisico]] in memoria
- **Dimensione**: il numero di bit del file
- **Protezione**: informazioni relative ai vari **permessi** sul file
- **Tempo**, data e identificazione dell'utente

Le **operazioni primitive** permesse da un [[Sistema operativo|SO]] sono:
- **Creazione**: alloca uno spazio di memoria sul disco dove verranno salvati i dati del file
- **Scrittura**: salva i nuovi dati del file (richiede un puntatore all'area di memoria su cui scrivere)
- **Lettura**: preleva i dati del file dalla memoria (richiede un puntatore all'area di memoria da cui leggere)
- **Riposizionamento**: modifica la posizione del puntatore all'interno del file
- **Cancellazione**: rimuove i dati e gli attributi del file e libera lo spazio in memoria
- **Troncamento**: mantiene gli attributi ma rimuove tutti i dati del file
- **Apertura**: copia il file dalla memoria secondaria a quella [[Memoria primaria|primaria]]
- **Chiusura**: libera la memoria primaria occupata dal file

---

Esistono diverse tipologie di accesso ad un file in memoria:
- **Sequenziale**: permette
	- lettura dei dati dopo il cursore
	- scrittura dei dati dopo il cursore
	- riposizionare il cursore all'inizio del file
	Non è permessa la riscrittura
- **Diretto**: permette
	- lettura da una certa posizione
	- scrittura da una certa posizione
	- riposizionare il cursore in uno specifico punto del file
	- tutte le operazioni permesse dall'accesso sequenziale
	- la riscrittura da una certa posizione