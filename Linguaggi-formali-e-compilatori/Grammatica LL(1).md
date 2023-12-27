---
 Created: 2023-12-27 18:56
 Author: Antonio Gelain
 Aliases: []
 Tags: [linguaggi-formali-e-compilatori]
---

Una **grammatica LL(1)** è un particolare tipo di [[Grammatica libera|grammatica libera]] che utilizza i seguenti passaggi per essere analizzata:
- Si guardano le parole da sinistra a destra
- Si esegue una produzione *leftmost*
- Si guarda un solo [[Simbolo|simbolo]] (*non terminale*)

---

> [!INFO] Questo tipo di grammatica è **completamente deterministica**

Per analizzare questo tipo di grammatica si costruisce una [[Tabella di parsing|tabella di parsing]] e vi si applica un [[Algoritmo|algoritmo]] per ottenere la derivazione della stringa $w \iff w \in \mathcal{L(G)}$(oppure *error()*) dato $w$, la tabella $M$ precedentemente descritta e la grammatica $\mathcal{G}$

Per questo algoritmo vengono utilizzati:
- Un buffer che conterrà la parola con un terminatore `$`
- Una [[Pila|pila]] che andrà a contenere i simboli terminali e non, inizializzato con lo *start symbol* $S$ e il terminatore `$`

Poi si tiene traccia del simbolo corrente $b$ all'interno della parola $w\$$ e del simbolo alla cima dello stack $X$ (all'inizio pari allo start symbol $S$)

Fino a che $X \ne \$$, ossia finché non ho svuotato la pila:
- Se $X = b$ allora tolgo l'elemento dalla cima della pila e imposto $b$ al simbolo successivo nell'input buffer (equivale ad un *match* con un terminale nella parola)
- Se invece $X$ è comunque un terminale, allora deve essere che $X \ne b$, ma ciò produce un errore
- Se invece $X$ è un non-terminale allora è necessario verificare la tabella di top-down parsing in posizione $M[X, b]$
    - Se $M[X, b] = error$ questo significa che la tabella in quella posizione è vuota e quindi viene restituito `error()`
    - Se $M[X, b] = X \rightarrow Y_{1}, ..., Y_{k}$ e quindi è una produzione che verrà utilizzata per continuare la derivazione; viene rimosso l'elemento $X$ dalla testa della pile e viene inserito il *body* della produzione in **ordine inverso** (in modo che $Y_{1}$ sia l'elemento in cima allo stack)
- Infine aggiorna $X$ col nuovo elemento in cima alla pila

In pseudo-codice:
```
% Creo una pila e ci inserisco il simbolo terminatore e lo start symbol %
Stack tmp = Stack()
tmp.push($)
tmp.push(S)
% Prendo il primo simbolo dalla parola e dallo stack %
Symbol b = w$.firstSymbol()
Symbol X = tmp.top()

% Finché non ho ottenuto una derivazione valida della stringa %
while X != $ do
    % Se il simbolo corrente è uguale a quello nello stack lo rimuovo e passo a quello successivo %
    if X == b then
        tmp.pop()
        b = w$.nextSymbol()
    % Se il simbolo nello stack è un terminale diverso da quello corrente ritorno un errore %
    elif isTerminal(X) then
        error()
    % Se la cella nella tabella non presenta nessun elemento ritorno un errore %
    elif M[X, b] == error then
        error()
    % Se la cella nella tabella presenta una produzione aggiorno lo stack e proseguo %
    elif M[X, b] == X -> Y1, ..., Yk then
        output(X -> Y1, ..., Yk)
        tmp.pop()
        
        % I nuovi elementi vengono aggiunti allo stack al contrario, in questo modo il simbolo più a sinistra viene analizzato per primo rispettando le regole del parsing %
        for Yi in Yk,...,Y1 do
            tmp.push(Yi)
        done
    fi

    % Processo il carattere succesivo nello stack %
    X = tmp.top()
done
```
