---
title: "Motion Control"
excerpt: "(:it: in Italian) This board was designed in 2008 which a dsPIC Microchip controller can control 2 DC brushed motor with a velocity control. In addiction this board can communicate with the Navigation Board and with a home made communication system send telemetry information to a remoted PC. The evolution of this board is μNAV!"
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2007
header:
  teaser: /assets/project/motion-control/MotionControlParticolare.jpg
---

Per gestire tutti i sottosistemi di regolazione, è stata sviluppata una scheda (denominata “Motion control”) che ha come base il microcontrollore dsPIC che implementa le leggi di controllo e gli algoritmi per l’elaborazione e comunicazione con la piattaforma di supervisione (in figura il rendering prima dello sviluppo della scheda).

{% include figure image_path="/assets/project/motion-control/Motion-Control-Top.jpg" alt="Rendering motion control" caption="Rendering motion control" %}

Un dsPIC, a differenza dei comuni microprocessori, che per poter funzionare hanno bisogno di numerosi integrati esterni aggiuntivi (ad esempio memoria, periferiche ed altro), si presenta completo di sistemi digitali programmabili racchiusi in un unico dispositivo, ovvero: una CPU (Central Processor Unit, unità centrale di elaborazione) la cui funzione è quella di interpretare le istruzioni di programma, una memoria di programma di tipo PROM, in cui sono memorizzate in maniera permanente le istruzioni del programma da eseguire, una memoria RAM utilizzata per memorizzare i dati di lavoro del programma, delle linee I/O per pilotare dispositivi esterni o per ricevere impulsi. Un dsPIC è dotato anche di un processore DSP, che è ottimizzato per eseguire in maniera estremamente efficiente sequenze di istruzioni ricorrenti (come ad esempio somme, moltiplicazioni e traslazioni), come nel condizionamento di segnali digitali, utilizzando un insieme di tecniche, tecnologie, algoritmi che permettono di trattare un segnale continuo dopo che è stato campionato.

La scheda Motion Control (in figura) oltre a disporre del microcontrollore, è predisposta per accogliere gli ingressi analogici e digitali provenienti dagli encoder e dal resto della strumentazione.

{% include figure image_path="/assets/project/motion-control/MotionControlCompleta.jpg" alt="Rendering motion completa" caption="Rendering motion completa" %}

Affinché tutte le operazioni di controllo e pianificazione del robot possano funzionare al meglio, è stato implementato sul microcontrollore uno scheduler che permette di pianificare le varie operazioni da eseguire nell’intervallo disponibile dalla CPU del microcontrollore.

Lo scheduler è l’elemento fondamentale per il corretto funzionamento del robot, gestione dei PID su ogni motore, odometria, letture dal campionatore, etc.

Il sistema è controllato da un timer che ne temporizza tutti gli eventi, basandosi sul clock di sistema. Esso è configurato per scadere ogni millisecondo e permettere quindi di avviare tutte le procedure di controllo richieste per il corretto funzionamento del robot.

Le funzioni sono schedulate in ordine di priorità in modo tale da permettere di eseguire tutte le funzioni richieste nel tempo richiesto.
1. Lettura parametri sensori
2. Calcolo odometria
3. Elaborazioni leggi di controllo (PID, regolazione cartesiana, etc etc)
4. Sincronizzazione dati su SPI

La Motion Control è costituita dal dsPIC33FJ128MC802, (nella figura, il particolare del microcontrollore saldato sulla scheda). Esso è un microcontrollore dalle elevate prestazioni (per una rapida consultazione se ne riportano le caratteristiche principali in tabella a fine pagina)

# Architettura interna

Il dsPIC33FJ128MC802 presenta un modulo CPU a 16-bit (data), con un set di istruzioni a 24-bit orientate al digital signal processing. Il Program Counter (PC) a 24-bit consente un indirizzamento fino a 4M x 24bit all’interno della memoria utente. La Program-Memory è di tipo Flash ed ha una capacità di 128KB. La Data-Memory è invece costituita da una RAM da 16KB.

Il modulo DSP-engine è costituito da un moltiplicatore 17bit x 17bit, da un’unità ALU a 40-bit, 2 accumulatori a 40-bit ed infine da due shifter in grado di effettuare su un valore a 40-bit, in un singolo ciclo, uno shift fino a 15-bit a destra e 16-bit a sinistra. La presenza di un PLL incrementa la frequenza interna di clock e consente di eseguire fino a 40 MIPs.

{% include figure image_path="/assets/project/motion-control/architetturadspic.jpg" alt="Architettura dspic" caption="Architettura dspic" %}

Si ricorda che l’esecuzione di ogni istruzione programma, richiede 2 cicli di clock dell’oscillatore (Fclk = Fosc=2, ad eccezione delle istruzioni che cambiano il flusso di esecuzione del programma e di quelle che lavorano direttamente sulle double-word).

Per quanto concerne la dotazione di periferiche hardware interne, il dsPIC33FJ128MC802 presenta: porte di interfacciamento I/O (le 3 porte A, B, C), 5 moduli Timer (Timer1/2/3/4/5 a 16-bit, con la possibilità da parte dei Timer2/3 e dei Timer 4/5 di lavorare a 32-bit in maniera congiunta), un modulo Input Capture, un modulo Output Compare (impostabile anche come PWM), moduli per l’interfacciamento seriale di tipo SPI, I2C e CAN, una periferica UART per la ricezione e la trasmissione seriale asincrona, una interfaccia di conversione dei dati DCI ed infine un convertitore A/D a 12-bit.

Sono inoltre presenti ulteriori caratteristiche atte a migliorare le funzionalità del sistema in termini di costi computazionali, aggiornabilità, stabilità e flessibilità. Tra tutte sono sicuramente da annoverare le opzioni per la selezione dell’oscillatore (tra cui la già menzionata attivazione del PLL interno), il Power-on reset (POR), il Watchdog Timer (WDT), la protezione per il codice (Code Protection) e la In-circuit Serial Programming (ICSP).

Rispetto alle serie precedenti, la famiglia di microcontrollori dsPIC33 utilizza il modulo DMA (Direct Memory Access) che ha il compito di gestire i dati passanti nel BUS, permettendo a periferiche che lavorano a velocità diverse di comunicare senza assoggettare la CPU a un enorme carico di interrupt.

Essenzialmente, in un trasferimento DMA, un blocco di memoria viene copiato da una periferica a un’altra. La CPU si limita a dare avvio al trasferimento, mentre il trasferimento vero e proprio è svolto dal controller DMA. Un caso tipico è lo spostamento di un blocco di memoria da unità di memoria esterna alla memoria principale. Se questa operazione, come avviene grazie al DMA, non blocca il processore, esso può continuare a svolgere altre operazioni.

# Caratteristiche

| Caratteristiche | Descrizione |
|-----------------|-------------|
| Package | SMD 28pin |
|Operating voltage range | 3.0V - 3.6V |
|Program Memory | 128KB |
|Timer 16-bit | 5 |
|QEI | 2 |
|UART | 2 |
|SPI | 2 |
|DMA | 8 canali hardware |

{% include figure image_path="/assets/project/motion-control/MotionControlParticolare.jpg" alt="Motion control particolare" caption="Motion control particolare" %}