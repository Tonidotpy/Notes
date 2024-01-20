---
 Created: 2023-12-29 18:45
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

L'[[Algoritmo|algoritmo]] di **shift/reduce** è un procedimento che permette di ottenere il [[Analisi sintattica|parsing]] di una parola $w$ data una [[Tabella di parsing bottom-up|tabella di parsing bottom-up]] di una certa [[Grammatica libera|grammatica]] $\mathcal{G}$

---

Per eseguire l'algoritmo è necessario inserire nell'input buffer la stringa $w\$$ e, inoltre, si ha bisogno di due [[Struttura di dati|strutture dati]]:
- Una [[Pila|pila]] degli [[Stato|stati]] $stSt$, che viene inizializzata ponendo in cima lo stato $P_{0}$
- Una pila dei [[Simbolo|simboli]] $symSt$

L'algoritmo in pseudo-codice è il seguente:
```
function bottomUpParsing(Word w, Table[][] M) begin
    b = il primo simbolo nell'input buffer
    % Inizializza stSt aggiungendo lo stato 0 %
    while true do
        % Sia S la cima di stSt %
        if M[S, b] = shift T then
            Push b onto symSt
            Push T onto stSt
            b = il prossimo simbolo nell'input buffer
        elif M[S, b] = reduce A -> b then
            Pop |b| symbol off symSt
            Push A onto symSt
            Pop |b| state off stSt
            % Sia tmp la cima di stSt %
            Push T onto stSt, where T is such that M[tmp, A] = goto T
            Output A -> b
        elif M[S, b] = ACCEPT then
            return
        else
            error()
        fi
    end
end
```

Nel caso in cui la traduzione tramite [[Grammatica attribuita|grammatica attribuita]] venga eseguita durante il parsing abbiamo bisogno di una terza pila per gli attributi $semSt$

Durante l'esecuzione dell'algoritmo se avviene un'operazione di:
- **Shift**: Si aggiunge l'attributo corrispondente al simbolo letto (*e.g.* se leggiamo il terminale $digit$ e il suo attributo identificato da $digit.lexval$ è `3`, si aggiunge `3` a $semSt$)
    Nel caso in cui il simbolo letto sia un terminale a cui non è associato alcun valore (ad esempio le operazione aritmetiche $+$, $\times$, $-$, $\div$) si aggiunge a $semSt$ un valore *fantoccio* che non modifica il risultato finale (ad esempio $0$ per la somma, $1$ per la moltiplicazione, ecc...)
- **Reduce**: Si rimuovono tanti attributi quanti sono i simboli nel body della riduzione, in $semSt$ e si aggiunge il corrispondente attributo ricavato dalla regola associata alla produzione della riduzione (*e.g.* se abbiamo una riduzione $T \rightarrow F$ e una regola associata $\{ T.val = F.val \}$, allora si rimuove l'attributo relativo a $F.val$ da $semSt$ e aggiungiamo il nuovo attributo identificato da $T.val$)

> [!IMPORTANT] Le operazioni descritte precedentemente funzionano solamente se l'SDD è **S-attribuita**
