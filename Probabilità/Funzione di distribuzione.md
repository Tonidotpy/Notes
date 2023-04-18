---
 Created: 2022-04-06 14:14
 Modified: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

# Funzione di distribuzione
*Def*: **Funzione di distribuzione** (o *funzione di ripartizione*):
1. **non decrescente**: $x \le y \Rightarrow F(x) \le F(y)$;
2. è **continua** a **destra**: $\lim_{x \to x_{0}} F(x) = F(x_{0)}\ \ \ \forall x_{0} \in \mathbb{R}$;
3. ammette il [[Limiti|limite]] a sinistra: $\exists \lim_{x \to x^{-}} F(x)\ \ \ \ \forall x_{0}\in \mathbb{R}$;
4. $\lim_{x \to -\infty} F(x) = 0$, $\lim_{x \to +\infty} F(x) = 1$.

---
$$P(\{(a, b]\}) = P(b) - P(a)$$

###### Tipi di funzione
- **Funzione di distribuzione uniforme** nell'intervallo $[0, 1]$ [^1];
	- Questo tipo di **funzioni di distribuzione** vengono chiamate (*assolutamente*)**continue**;
- **Funzione di distribuzione uniforme a scalini** [^2];
	- **Funzioni di distribuzione** che assegnano masse di probabilità ad una quantità al più numerabile di singoletti (*reali*) è chiamata **discreta**;
- **Funzione di distribuzione mista** [^3].

[^1]: ![Funzione di distribuzione uniforme|200](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/Grafico_v.c.uniforme.png/440px-Grafico_v.c.uniforme.png) [^2]: ![Funzione di distribuzione uniforme a scalini|300](https://www.webtutordimatematica.it/images/materie/statistica-e-probabilita/distribuzioni-di-probabilita-continue/densita-distribuzione-uniforme.png) [^3]: ![Funzione di distribuzione mista|300](https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/3_r%C3%A9partitions.png/400px-3_r%C3%A9partitions.png)

*Def*: una **funzione di distribuzione** è **assolutamente continua** se è una [[Funzione continua|funzione continua]] ed è [[Derivate|derivabile]] su tutto $\mathbb{R}$ tranne al più in una quantità numerabile di punti.
