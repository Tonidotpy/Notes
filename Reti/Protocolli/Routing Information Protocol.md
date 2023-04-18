---
 Created: 2022-12-28 17:18
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [RIP]
 Tags: [protocol]
---

**Routing Information Protocol** (*RIP*) è un protocollo di routing utilizzato per **instradare** i pacchetti di dati su reti di [[Computer|computer]]

---

Il protocollo RIP utilizza l'[[Algoritmo di Bellman-Ford|algoritmo di Bellman-Ford]] e perciò è semplice da implementare e gestire ma ha una convergenza lenta e una dimensione della rete limitata

Il costo dei link è pari al **numero di hop** che può essere al massimo 15 (un singolo hop può avere un costo maggiore di 1)
Ogni 30 secondi o se cambiano le [[Tabella di Routing|tabelle di routing]] RIP invia dei *"RIP advertisement"* ossia dei messaggi che contengono un elenco con fino a 25 sottoreti di destinazione dell'[[Autonomous System|AS]] e la distanza del mittente rispetto a ciascuna di tali sottoreti

RIP utilizza il protocollo [[User Datagram Protocol|UDP]] con porta `520` e [[Indirizzo di multicast|indirizzo di multicast]] `224.0.0.9`

Se un [[Router]] non riceve notizie dal suo vicino per `180 s` il collegamento viene considerato **guasto** e RIP provvede a **modificare** la tabella di instradamento locale e **propagare** l'aggiornamento ai router vicini