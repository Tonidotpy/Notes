---
 Created: 2022-12-29 19:02
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [MAC]
 Tags: []
---

Il **Media Access Control** (*MAC*) è un sottolivello del livello di [[Livello di collegamento|data link]] di un sistema di elaborazione che si occupa della **gestione** dell'accesso al mezzo di trasmissione, ovvero della gestione della **condivisione** della rete fisica da parte di più dispositivi

---

Lo scopo di questo sottolivello è di permettere ad `N` dispositivi di **comunicare** attraverso un canale in comune a tutti con velocità di trasmissione `R`, ad una **velocià media** il più possibile vicina a `R/N` tramite un controllo **semplice** e **decentralizzato**

Esistono tre **classi** per la suddivisione delle risorse:
- A **ripartizione delle risorse** di canale dove il canale viene suddiviso in più parti allocate in modo esclusivo ad ogni dispositivo:
	- [[Time Division Mutliple Access|TDMA]]
	- [[Frequency Division Mutliple Access|FDMA]]
	- [[Code Division Mutliple Access|CDMA]]
- Ad **accesso casuale** in cui l'intero canale non viene suddiviso e si cerca di minimizzare le collisioni:
	- [[ALOHA]]
	- [[Slotted ALOHA]]
	- [[Carrier Sense Multiple Access|CSMA]]
	- [[Carrier Sense Multiple Access Collision Detection|CSMA/CD]]
	- [[Carrier Sense Multiple Access Collision Avoidance|CSMA/CA]]
- A **turni intelligenti** in cui i nodi accedono *a turno* dando priorità a quelli che devono trasmettere più dati:
	- [[Protocollo di polling]]
	- [[Token passing]]