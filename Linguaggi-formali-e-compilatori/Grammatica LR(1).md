---
Created: 2023-12-30 17:00
Author: Antonio Gelain
aliases:
  - Grammatica Left Rightmost(1)
tags:
  - linguaggi-formali-e-compilatori
---

Una **grammatica LR(1)** è un tipo di [[Grammatica libera|grammatica libera]] utilizzato per rendere più efficiente il [[Bottom-Up parsing|parsing bottom-up]]

---

Gli [[Stato|stati]] dell'[[Automata|automa]] caratteristico di una grammatica LR(1) vengono chiamati *LR(1)-items* e hanno la seguente forma:
$$[ A \rightarrow \alpha \cdot B \beta, \Delta ] \text{ dove } \Delta \subseteq T \cup \{ \$ \}$$

> [!INFO] L'[[Analisi/Insiemi/Insieme|insieme]] di caratteri $\Delta$ viene chiamato ***lookahead set***

## Chiusura di un insieme di LR(1)-item

La prima cosa da fare per calcolare una $closure_{1}(item)$ è di calcolare la sua $closure_{0}(item)$ utilizzando la parte [[Grammatica LR(0)#Chiusura di un insieme di LR(0)-items|LR(0)]] dell'item LR(1) che stiamo chiudendo

Successivamente si aggiorna l'insieme di *lookahead*, che viene aggiunto alla $closure_{0}(item)$ appena calcolata

Dato $P$ un insieme di LR(1)-items, la $closure_{1}(P)$ identifica **il più piccolo** insieme di item, con **il più piccolo** *lookahead-set*, che soddisfa la seguente equazione:
$$closure(P) = P \cup \{ [B \rightarrow \cdot \gamma, \Gamma] : [A \rightarrow \alpha \cdot B \beta, \Delta] \in closure_{1}(P) \land B \rightarrow \gamma \in \mathcal{P'} \land first(\beta \Delta) \subseteq \Gamma \}$$
dove $first(\beta \Delta) = \bigcup_{d \in \Delta} first(\beta d)$ e $\mathcal{P}'$ è ricavato dall'insieme delle [[Produzione|produzioni]] $\mathcal{P}$ aggiungendo la produzione $S' \rightarrow S$

In pseudo-codice:
```
function closure1(Set P) -> Set begin
    % Setta ogni item in P come unmarked %
    while esiste item in P : item è unmarked do
        mark(item)
        if item è nella forma [A -> a * B b, D] then
            D1 = U_{d in D} first(bd)
            foreach B -> y in P' do
                % Controllo se l'item B -> *y è presente in closure1(P) o meno %
                if B -> *y not in prj(P) then
                    add [B -> *y, D1] to P as unmarked item
                else
                    if [B -> *y, Y] in P and D1 not subset Y then
                        Update [B -> *y, Y] to [B -> *y, Y U D1] in P
                        Tag [B -> *y, Y U D1] as unmarked
                    fi
                fi
            done
        fi
    done
    return P
end
```

## Costruzione dell'automa caratteristico

Per costruire l'[[Automata|automa]] caratteristico si deve:
1. Costruire lo stato di partenza con l'item $[S' \rightarrow \cdot S, \$]$
2. Si aggiungono ricorsivamente gli stati che si possono raggiungere dagli stati presenti nell'automa
3. Si aggiungono le transizioni che ci permettono di passare da uno stato ad un altro

Una transizione da uno stato $P$ ad un altro stato $Q$ esiste se $P$ contiene un item nella forma $[A \rightarrow \alpha \cdot Y \beta, \Delta]$; a sua volta anche $Q$ contiene quell'item e tutti gli item in $closure_{1}([A \rightarrow \alpha Y \cdot \beta, \Delta])$

In pseudo-codice:
```
function LR(1)-automatonConstruction(Grammar G) begin
    % Inizializzo la collezione Q con P0 = closure1({[S' -> *S, {$}]}) %
    % Setto P0 come unmarked %
    while esiste uno stato P in Q : P è unmarked do
        mark(P)
        foreach Y sulla destra del marker in un qualche item di P do
            % Calcolo in tmp il kernel-set dell'Y-target di P %
            if Q contiene uno stato R il cui kernel è tmp then
                % Sia R l'Y-target di P %
            eles
                Add closure1(tmp) a Q come stato unmarked
                % Sia closure1(tmp) l'Y-target di P %
            fi
        done
    done
end
```
