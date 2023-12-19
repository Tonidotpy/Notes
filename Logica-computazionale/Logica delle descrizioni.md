---
Created: 2023-12-11 11:28
Author: Antonio Gelain
aliases:
  - LOD
tags:
  - logica-computazionale
---

La **logica delle descrizioni** (o *LOD*) ci permette di ragionare sui concetti e le regole che descrivono le [[Entità|entità]] nel mondo
$$\text{LOD} = \langle \text{ETG}, \models_{\text{LOD}} \rangle$$
con
$$\text{ETG} = \langle L_{\text{LOD}}, D_{\text{LOD}}, I_{\text{LOD}} \rangle$$

---

Nel LOD abbiamo is seguenti elementi:
- Un [[Tipo entità|tipo entità]] (*etype*); è una classe di entità
- Un [[Tipo di dato|tipo di dato]] (*dtype*); è una classe di valori ([[Dato|dati]])
- Una proprietà di un oggetto; che descrive una relazione tra due *etypes*
- Una proprietà di un dato (o *attributo*); che descrive una caratteristica di un *etype*

---

Nella [[Dominio di interpretazione|definizione intensionale del dominio]] abbiamo che:
- $E$ è un insieme di entità e valori: $E = \{ e \} \cup \{ v \}$
- $\{ C \}$ è un insieme di etype e dtype: $\{ C \} = ET \cup DT$
- $\{ R \}$ è un insieme di oggetti e relazioni tra dati