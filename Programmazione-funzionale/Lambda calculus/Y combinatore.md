---
 Created: 2022-06-19 13:32
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Y combinatore
L'**$Y$ combinatore** è una [[Lambda calculus|espressione lambda]] senza **variabili libere** che data una **funzione** come argomento ne restituisce un'altra ed è definita come:
$$Y = \lambda f.(\lambda x.f(xx))(\lambda x.f(xx))$$

Dalla definizione possiamo ricavare che:
$$Y e = e(Y e)$$
di conseguenza sappiamo che $Y e$ è un [[Combinatore a punto fisso|fixpoint]] per $e$ perciò possiamo utilizzare la **ricorsione** tramite una valutazione per **nome** (per **valore** si ha una **ricorsione infinita**).