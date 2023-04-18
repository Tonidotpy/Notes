---
 Created: 2022-06-16 11:44
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Macchine astratte
Le **macchine astratte** sono una collezione di algoritmi e strutture dati che permettono di **memorizzare** ed **eseguire** programmi come in una [[Macchine fisiche|macchina fisica]].

Data una **macchina astratta** $\mathcal{M_L}$ essa può capire ed eseguire programmi scritti nel linguaggio $\mathcal{L}$.

###### Operazioni
Per eseguire operazioni in $\mathcal{L}$, $\mathcal{M_L}$ deve:
1. eseguire operazioni elementari;
2. controllare la sequenza di di esecuzione;
3. trasferire i dati da e alla memoria;
4. organizzare la memoria.

###### Implementazione nel software
Il software viene eseguito in una [[Macchine fisiche|macchina fisica]] $\mathcal{MO_{LO}}$ (con linguaggio $\mathcal{LO}$, $\mathcal{P^{L}: D \mapsto D}$) e può essere:
- **Interpretato**: un programma scritto in $\mathcal{LO}$ ne comprende ed esegue uno scritto in $\mathcal{L}$ -> $\mathcal{I^{LO}_{L}: (PR^{L} \times D) \mapsto D}$;
	- è meno efficiente;
	- è più flessibile e portabile;
	- il debugging è più semplice;
- **Compilato**: un programma ne traduce un altro da $\mathcal{L}$ a $\mathcal{LO}$ -> $\mathcal{C^{LA}_{L, LO}: PR^{L} \mapsto PR_{LO}}$;
	- è molto efficiente;
	- è più complesso e meno portabile;
	- il debugging è generalmente più difficile;
- **Ibrido**: un programma ne *compila* un altro da $\mathcal{L}$ in un *linguaggio intermedio* $\mathcal{LI}$ che viene successivamente *interpretato* da una macchina $\mathcal{MO_{LO}}$ scritta in $\mathcal{LI}$.