---
 Created: 2023-09-26 17:35
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

Il meccanismo di **bit banding** permette di eseguire un'istruzione di caricamento o salvataggio in [[Memoria|memoria]] su un **singolo bit** anziché su un intero gruppo

---

Ogni bit presente nell'area di memoria dedicata al *bit banding* viene referenziato da un indirizzo **multiplo di 4*

```c
bit_wordd_addr = bit_band_base + (byte_offset * 32) + (bit_number * 4)
```

Il meccanismo di bit banding permette un esecuzione di operazioni sui bit più efficienti per via del minor numero di istruzioni utilizzate e permettono di ottenere [[Operazione atomica|operazioni atomiche]]