---
 Created: 2022-12-09 20:59
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Lo **pseudo-codice** è una **notazione informale** utilizzata per descrivere un **algoritmo** o un procedimento in modo che sia facilmente comprensibile anche da chi non è un esperto di programmazione

---

## Notazione

###### Inizializzare una variabile
```c++
a = b
```
###### Scambiare due variabili
```c++
a ↔ b
```
che equivale a:
```c++
tmp = a;
a = b;
b = tmp;
```

###### Inizializzare un array di $n$ elementi
```c++
T[] A = new T[1...n]
```
###### Inizializzare una matrice $n \times m$
```c++
T[][] B = new T[1...n][1...m]
```
###### Tipi primitivi
```c++
int, float, boolean, int
```
###### Operatori booleani
```c++
and, or, not
```
###### Uguaglianze e disequazioni
$$==,\ \ne,\ \ge,\ \le$$
###### Operazioni
$$+,\ -,\ \cdot,\ /,\ \lfloor x \rfloor,\ \lceil x \rceil,\ \log,\ x^{2},\ ...$$
###### Selezione condizionale
```c++
iif(condizione, v1, v2)
```
###### Blocchi condizionali
```c++
if condizione then istruzione

if condizione then istruzione1
else istruzione2
```
###### Blocchi iterativi
```c++
while condizione do istruzione

foreach element ∈ insieme do istruzione
```
###### Return keyword
```c++
return
```
###### Commenti
```c++
% commento
```