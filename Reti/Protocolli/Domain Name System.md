---
 Created: 2022-12-18 20:52
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: [DNS]
 Tags: [protocol]
---

**Domain Name System** (*DNS*) è un protocollo utilizzato per **tradurre** gli indirizzi web (come ad esempio [www.example.com](http://www.example.com)) in [[Internet Protocol versione 4|indirizzi IP]], che sono utilizzati dai [[Computer|computer]] per **identificare univocamente** i dispositivi su una rete, come ad esempio Internet

---

La struttura che utilizza il DNS non è altro che un enorme **database distribuito** implementato in una gerarchia di *server DNS* che permette di *risolvere* i nomi (ossia **tradurre** indirizzi/nomi)

Il DNS offre diversi **servizi** come:
- **Traduzione** degli *hostname* in [[Internet Protocol versione 4|indirizzi IP]]
- ***Host aliasing***: ossia tradurre **nomi diversi** nello stesso indirizzo
- ***Mail server aliasing***
- **Distribuzione del carico**

La struttura dei server DNS è **gerarchica** con dei server **radice** alla cima che sono collegati a dei server di **dominio** che a loro volta sono collegati a server di **sottodominio** e così via

![[DNS-servers-hierarchy.png]]

Al momento esistono 13 server radice *logici* sparsi per il mondo

Al di sotto dei server radice si trovano quelli di **top-level-domain** (o *TLD*) che si occupano dei **domini** (*com*, *org*, *net*, *edu*, ecc...) e di tutti i **domini locali** di **alto livello** (*it*, *uk*, *fr*, *ca*, *jp*, ecc...)
Ogni organizzazione dotata di host Internet pubblicamente accessibili deve fornire dei record DNS attraverso dei **server di competenze** (*authoritative server*)

Ciascun [[Internet Service Provider|ISP]] ha un suo server DNS **locale** che fa da tramite per i server DNS di più alto livello

---

Una volta che un server DNS impara la mappatura, la mette nella *cache* e le informazioni vengono **invalidate** dopo un certo periodo di tempo

Il protocollo DNS salva dei **Resource Record** (*RR*), che sono delle informazioni necessarie per la **risoluzione dei nomi**

I RR sono formati da:
- `name`
- `value`
- `type`
- `ttl` o **Time To Live**

Esistono 4 tipi di RR:
1. **Tipo A** o *Authoritative*
	- `name` è il nome dell'host
	- `value` è il suo [[Internet Protocol versione 4|IP]]
2. **Tipo NS** o *Name Server*
	- `name` è il dominio
	- `value` è il nome dell'host del server di competenza del dominio
3. **Tipo CNAME** o *Canonic NAME*
	- `name` è il nome *alias* rispetto al nome vero
	- `value` è il nome reale, detto anche *canonico*
4. **Tipo MX** o *Mail eXchange*
	- `value` è il nome del server di posta associato a `name`

---

I messaggi del protocollo DNS sono delle **domande** (*query*) o **risposte** con lo stesso formato:
- **Intestazione**
	- **Identificazione**: un numero di 16 bit per la domanda/risposta
	- **Flags**
		- domanda o risposta
		- richiesta di ricorsione
		- ricorsione disponibile
		- risposta di competenza
	- **Numero di domande**
	- **Numero di risposte**
	- Numero di RR autorevoli
	- Numero di RR addizionali
- **Dati**
	- **Domande**
	- **Risposte**
	- Competenza
	- Informazioni aggiuntive

![DNS-message](http://www.programmiamo.altervista.org/internet/immagini/imgE.jpg)