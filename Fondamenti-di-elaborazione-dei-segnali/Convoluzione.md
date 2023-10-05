---
 Created: 2023-10-04 13:51
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

La **convoluzione** è un'operazione tra due [[Funzione|funzioni]] di una variabile che consiste nell'utilizzo dell'[[Integrale di convoluzione|integrale di convoluzione]]

---

Tramite la convoluzione è possibile determinare la risposta all'[[Delta di Dirac|impulso]] di un [[Sistema lineare tempo-invarianti|sistema LTI]]

La convoluzione restituisce una funzione che ha durata pari alla somma delle durate dei due [[Segnale|segnali convoluti]]

>[!INFO] La convoluzione è un'operazione **lineare** e gode delle proprietà [[Associatività|associativa]], [[Commutatività|commutativa]] e [[Distributività|distributiva]]

## Convoluzioni notevoli

### Convoluzione con impulsi

Una convoluzione di un segnale con un impulso restituisce il segnale stesso (sistema **passa-tutto**)
$$x(t) * \delta(t) = x(t)$$

Se invece eseguo la convoluzione con un impulso traslato, ottengo la traslazione del segnale della stessa quantità (sistema di **ritardo**)
$$x(t) * \delta(t - T) = x(t - T)$$

### Convoluzione con rettangoli simmetrici di pari durata

In pratica, il rettangolo che trasla agisce come una finestra di integrazione mobile rispetto a quello fisso, perciò otteniamo un **segnale triangolare**:
$$x_{1}(t) * x_{2}(t) = A_{1}A_{2}T\left(1 - \frac{|t|}{T}\right) \text{ in } [-T, +T] = A_{1}A_{2}T \Lambda \left(\frac{t}{2T}\right)$$

### Convoluzione con rettangoli simmetrici di diversa durata

Dalla convoluzione tra due rettangoli simmetrici di diversa durata si ottiene un **trapezio simmetrico** rispetto all'origine
$$x_{1}(t) * x_{2}(t) = \int_{t - \frac{T_{2}}{{2}}}^{\frac{T_{1}}{2}} A_{1}A_{2} d\tau = A_{1}A_{2}\left(\frac{T_{1} + T_{2}}{2} - t\right)$$

### Convoluzione con rettangoli non simmetrici

Il caso dei rettangoli non simmetrici si può estrapolare a partire dai casi precedenti grazie alle proprietà della convoluzione, perciò la forma d'onda è uguale ma subisce la somma dei ritardi

### Convoluzione con gaussiane

Consideriamo due [[Variabile aleatoria normale|gaussiane]] con diverse medie e varianze
La convoluzione di queste due gaussiane è pari alla seguente formula che restituisce una nuova gaussiana con [[Valore medio di un segnale|valore medio]] pari alla somma dei valori medi, e [[Varianza di un segnale|varianza]] pari alla somma delle varianze
$$y(t) = x_{1}(t) * x_{2}(t) = \frac{1}{\sqrt{2 \pi (\sigma_{1}^{2} + \sigma_{2}^{2})}} e^{-\frac{[t - (\mu_{1} + \mu_{2})]^{2}}{2 (\sigma_{1}^{2} + \sigma_{2}^{2})}}$$

