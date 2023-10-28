---
 Created: 2021-10-28 09:58
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: [matematica,analisi,funzioni]
---

# Funzione

Una **funzione** è una [[Relazione|relazione]] che associa ad ogni elemento di un [[Analisi/Insiemi/Insieme|insieme]] di partenza $A$ **uno e un solo** elemento di un [[Analisi/Insiemi/Insieme|insieme]] di arrivo $B$.
$$f: A \mapsto B$$

---

## Caratteristiche

### Suriettività

Una funzione $f$ si dice **suriettiva**(o *surgettiva*) se, ogni elemento di del [[Codominio|codominio]] è un [[Immagine|immagine]] di alcuni elementi del [[Dominio|dominio]]
$$\forall b \in B, \exists a \in A\ |\ f(a) = b$$

### Iniettività

Una funzione $f$ si dice **inettiva** se diversi elementi del dominio hanno **immagini distinte** nel codominio:
$$\forall b \in \text{Im}_{f}, \exists! a \in A\ |\ f(a) = b$$

### Biettività

Una funzione $f$ si dice **biettiva**(o *bigettiva*) quando $f$ è sia iniettiva che suriettiva:
$$\forall b \in B, \exists! a \in A\ |\ f(a) = b$$