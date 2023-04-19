---
 Created: 2023-04-19 10:23
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Un **thread** è una suddivisione di un [[Processo|processo]] in due o più sottoprocessi che vengono eseguiti **concorrentemente**

---

I thread di un processo condividono lo stesso **spazio di indirizzamento**, **risorse** e **stato** del processo
La possibilità di un sistema di supportare più thread viene chiamata **multi-threading**

L'utilizzo del multi-threading permette di:
- **Ridurre** il tempo di risposta di un processo
- **Condividere** le risorse
- Utilizzare **meno risorse** per il [[Context switching|context switching]]
- Semplificare la **scalabilità** del sistema

Esistono due tipi di thread:
1. **User-level** thread:
	- La gestione viene affidata alle applicazioni
	- Il [[Kernel|kernel]] ignora l'esistenza dei thread
	- Le funzionalità sono disponibili tramite una libreria
2. **Kernel-level** thread:
	- La gestione viene affidata al kernel
	- Le applicazioni utilizzano i thread tramite [[Sistema operativo#^90bd2d|system calls]]