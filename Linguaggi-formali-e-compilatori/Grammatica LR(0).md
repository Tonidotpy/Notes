---
Created: 2023-12-29 14:12
Author: Antonio Gelain
aliases:
  - Grammatica Left Rightmost(0)
tags:
  - linguaggi-formali-e-compilatori
---

Una **grammatica LR(0)** è un tipo di [[Grammatica libera|grammatica libera]] utilizzato per rendere più efficiente il [[Bottom-Up parsing|parsing bottom-up]]

---

Gli [[Stato|stati]] dell'[[Automata|automa]] caratteristico di una grammatica LR(0) vengono chiamati *LR(0)-items* e hanno la seguente forma:
$$A \rightarrow \alpha \cdot \beta$$

## Chiusura di un insieme di LR(0)-items

Dato $P$ un [[Analisi/Insiemi/Insieme|insieme]] di LR(0)-items definiamo $closure_{0}(P)$ come il più piccolo insieme che soddisfa la seguente equazione:
$$closure_{0}(P) = P \cup \{ B \rightarrow \cdot \gamma\ |\ A \rightarrow \alpha \cdot B \beta \in closure_{0}(P) \land B \rightarrow \gamma \in P' \}$$

Per calcolare la **chiusura** di $P$ è quindi necessario includere **ricorsivamente** tutte le [[Produzione|produzioni]] che presentano un *marker* ($\cdot$) prima di un non-terminale

In pseudo-codice:
```
function chiusura0(Set P) -> Set begin
    % Setto ogni item come unmarked %
    foreach item in P do
        % Etichetta item come unmarked %
    done

    % Per ogni item non marcato %
    while esiste item in P : item è unmarked do
        mark(item)

        % Se l'item corrente ha la forma A -> a * Bb %
        if item ha forma A -> a * Bb then
            foreach B > y in P' do
                if B -> *y not in P then
                    % Aggiungi B -> *y a P come unmarked item %
                fi
            done
        fi
    done
    return P
end
```

## Costruzione dell'automa caratteristico

All'inizio si definisce il *kernel* dello stato iniziale come $P_{0} = \{ S' \rightarrow \cdot S \}$, dove $S'$ è un carattere nuovo non presente nella grammatica iniziale, mentre $S$ è lo *start-symbol* della grammatica

Finché non esauriamo tutti gli stati ancora da visitare:
- Si calcola la chiusura del *kernel* dello stato, questo insieme rappresenta tutte le produzioni che si possono compiere da un certo stato per transitare verso altri stati
- Una volta calcolata la chiusura, le produzioni (gli *item*) che abbiamo già collezionato avranno forma $A \rightarrow \alpha \cdot x \beta$, il che significa che nello stato in cui mi trovo $P$, ho già visto $\alpha$ e posso fare una transizione tramite $x$
- Esiste quindi una transizione da $P$ ad un altro stato $P'$ attraverso l'item $A \rightarrow \alpha x \cdot \beta$; se $x$ è un terminale, tale transizione rappresenta un'operazione di [[Shift-Reduce|shift]], questo significa che avrò una transizione etichettata con $x$ che mi porta da $P$ a $P'$
- A questo punto genero il nuovo stato $P'$ che contiene come *kernel* l'item $A \rightarrow \alpha x \cdot \beta$
Nel caso in cui un *kernel* di un nuovo stato $P'$ sia uguale ad uno già presente $Q$, invece di generare il nuovo stato si aggiunge una $x$-transizione a $P$ a $Q$ 

In pseudo-codice:
```
function charAutomataConstruction(Grammar G) begin
    % Inizializzo Q in modo che contenga P0 = chiusura0({ S' -> S }) %
    % Etichetto P0 come unmarked %
    while esiste P in Q : P è unmarked do
        mark(P)
        foreach Y a detra del marker in qualche item di P do
            % Calcolo il kernel-set tmp per lo stato bersaglio della Y-transizione che parte da P %
            if Q contiene uno stato Q di kernel tmp then
                % Sia Q lo stato bersaglio della Y-transizione che parte da P %
            else
                % Aggiungo chiusura0(tmp) a Q come stato unmarked %
                % Sia chiusura0(tmp) lo stato bersaglio della Y-transizione che parte da P %
            fi
        done
    done
end
```