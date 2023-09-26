---
 Created: 2023-09-18 21:40
 Author: Antonio Gelain
 Aliases: []
 Tags: []
---

**Cortex-M4** è un tipo di [[Processore|processore]] con [[Architettura|architettura]] [[Advanced RISC Machine|ARM]] basata su *Armv7E-M* che offre elevate prestazioni è diverse funzionalità avanzate

---

Questo tipo di processo è stato progettato per:
- Un'elevata efficienza nella gestione ed **elaborazione dei segnali**
- Consumi energetici ridotti
- Maggior affidabilità tramite **determinismo**

Utilizza l'[[Architettura Harvard|architettura Harvard]] è supporta completamente i set di istruzioni [[Thumb Instruction Set|Thumb]] e il [[Thumb-2 Instruction Set|Thumb-2]]

Supporta inoltre le cosiddette *sleep modes* ossia i [[Interrupt|wake-up interrupt]] e istruzioni avanzate come la divisione lato [[Hardware|hardware]]

## Block diagram

![cortex-m4-block-diagram](https://www.researchgate.net/publication/329628732/figure/fig2/AS:703426174398465@1544721277353/Cortex-M4-kernel-block-diagram-and-minimum-system-circuit.ppm)

Il [[Processore|processore]] utilizza una [[Pipelining|pipeline]] a **tre fasi**: *fetch*, *decode* e *execution* che permette di eseguire istruzioni diverse con una maggiore efficienza rispetto ad un processore senza pipeline mantenendo l'architettura del processore molto semplice

I [[Registro|registri]] di un processore cortex-m4 sono suddivisi in:
- **Banco di registri**:
    - Registri *general purpose*
    - [[Stack Pointer]]
    - [[Link Register]]
    - [[Program Counter]]
- **Registri speciali**:
    - [[Program Status Register]]
    - [[Internal Mask Register]]

## Memory map

![cortex-m4-memory-map](https://microcontrollerslab.com/wp-content/uploads/2020/07/Memory-Map-region-TM4C123GH6PM-arm-cortex-M4.jpg)

L'area dedicata al [[Codice|codice]] viene principalmente salvata su una [[Memoria flash|memoria flash]] integrata nel chip mentre nella [[Static Random Access Memory|SRAM]] vengono salvati i dati dello [[Stack|stack]] e dell'[[Heap|heap]], ma può essere utilizzata anche per il codice

Per alcune sezioni di memoria sono presenti delle regioni dedicate esclusivamente al [[Bit banding|bit banding]]