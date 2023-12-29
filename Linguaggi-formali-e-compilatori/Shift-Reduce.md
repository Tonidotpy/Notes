---
 Created: 2023-12-29 18:45
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

L'[[Algoritmo|algoritmo]] di **shift/reduce** è un procedimento che permette di ottenere il [[Analisi sintattica|parsing]] di una parol $w$ data una [[Tabella di parsing bottom-up|tabella di parsing bottom-up]] di una certa [[Grammatica libera|grammatica]] $\mathcal{G}$

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
