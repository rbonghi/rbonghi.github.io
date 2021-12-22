---
title: "Roboduck"
excerpt: "(:it: in Italian) This robot controlled by a 18F4500 microchip could be obstacle avoidance little obstacle and walk autonomously."
permalink: /robot/roboduck
classes: wide
number: 2006
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  teaser: /assets/robot/rodobuck/roboduck-front.jpg
  overlay_image: /assets/robot/rodobuck/roboduck-walk.jpg
roboduck1:
  - url: /assets/robot/rodobuck/roboduck-weights.jpg
    image_path: /assets/robot/rodobuck/roboduck-weights.jpg
    alt: "Roboduck pesi"
    title: "Roboduck pesi"
  - url: /assets/robot/rodobuck/roboduck-no-batteries.jpg
    image_path: /assets/robot/rodobuck/roboduck-no-batteries.jpg
    alt: "Roboduck senza batterie"
    title: "Roboduck senza batterie"
roboduck2:
  - url: /assets/robot/rodobuck/roboduck-walk.jpg
    image_path: /assets/robot/rodobuck/roboduck-walk.jpg
    alt: "Roboduck laterale"
    title: "Roboduck laterale"
  - url: /assets/robot/rodobuck/roboduck-front.jpg
    image_path: /assets/robot/rodobuck/roboduck-front.jpg
    alt: "Roboduck front"
    title: "Roboduck front"
roboduck3:
  - url: /assets/robot/rodobuck/roboduckScheda.jpg
    image_path: /assets/robot/rodobuck/roboduckScheda.jpg
    alt: "Roboduck scheda - rendering"
    title: "Roboduck scheda - rendering"
  - url: /assets/robot/rodobuck/roboduck-walk.jpg
    image_path: /assets/robot/rodobuck/roboduck-walk.jpg
    alt: "Roboduck camminata"
    title: "Roboduck camminata"
---

Roboduck nasce nell'agosto del 2007 tra un esame ed un altro in una calda estate, l'obiettivo era quello di realizzare un piccolo robot camminatore dall'altezza di 11 cm. Venne progettato usando come sistema di locomozione 2 Servomotori S75 E-flite (simili agli HITEC HS-48) ed una meccanica totalmente in legno.

{% include figure image_path="/assets/robot/rodobuck/roboduck-firstversion.jpg" alt="Roboduck prima versione" caption="Roboduck prima versione" %}

L'idea del progetto era di costruire un semplice telaio usando materiali poco costosi quali il legno per realizzare la struttura meccanica del piccolo robot.  Il sistema è costituito da un motore che permette alle due "zampe" di "dis-allinearsi" ed un secondo motore che fa alzare e reciprocamente abbassare le zampe del robot, combinando i due movimenti, il robot può camminare facendo assomigliare il suo movimento a quello di una papera.

{% include gallery id="roboduck1" caption="Struttura roboduck" %}

Durante la prima realizzazione si capì che un solo sostegno per la sorreggere la "zampa" del robot non era sufficiente per mantenere in equilibrio il robot. Risultò necessario riprogettare il la meccanica ed integrare nel sistema di movimentazione del robot un secondo sostegno com'è visibile nella figura. La difficoltà nella realizzazione del robot consisteva nel riuscire a lavorare con precisione il legno delle sue varie parti.

Le dimensioni del robot rimangono quindi inalterate rispetto alla precedente versione e si riesce ad avere una dimensione complessiva relativamente piccola del robot:
* 11cm Altezza
* 5cm profondità
* 9,5cm larghezza

Una volta ultimato il telaio e verificato il corretto funzionamento si è reso necessario trovare la corretta disposizione delle batterie del robot cercando di garantire comunque l’equilibrio del robot in fase di camminata ed eviare possibili sbilanciamenti. La disposizione più corretta è risultata quindi quella di avere le batterie disposte lateralmente.

{% include gallery id="roboduck2" caption="Struttura roboduck" %}

Il robot grazie all’elettronica di controllo assicura di potersi muovere evitando gli ostacoli presenti in traiettoria, grazie infatti a due piccoli sensori infrarossi posti proprio sulla “testa” del robot.

# Scheda di controllo

La scheda di controllo è costituita da un microcontrollore della serie 18F prodotta dalla microchip. Sulla scheda è stato predisposto un sistema di connettori tali da garantire il corretto montaggio dei servocomandi ed è stato inserito anche un potenziometro analogico ed un pulsante in modo tale da poter essere configurato il robot in modo tale da poter essere calibrato o per testare altre strategie di movimento.

Le specifiche complessive della scheda elettronica e dei vari componenti del robot sono elencate qui di seguito:
* Dimensioni: 4x4,5cm (componenti in SMD)
* PIC18F2520 ad una frequenza di 40Mhz (10Mips)
* Programmazione ICSP
* Alimentazione da: 5.01V a 24V (sarà alimentata con una Lipo da 7,5V 340mA)
* Uscita per controllo attraverso porta Seriale
* Sensori On-Board (infrarossi)
* Trimmer digitale integrato
* Sensore controllo carico batteria
* 2 Led (rosso e blu)
* Pulsante Digitale
* Porte libere per possibili espansioni

{% include gallery id="roboduck3" caption="Roboduck scheda" %}

Un dettaglio del robot Roboduck in funzione, si può notare la posizione non in asse delle due zampe del robot.

# Video

Il video del robot roboduck in funzione, mostra come la camminata è regolare e riesce comunque a muoversi dritto su una superficie liscia.

{% include video id="Xel_fhoFtGY" provider="youtube" %}

Nel secondo video, si vede come il robot evita gli ostacoli.

mentre nell'ultimo video il robot prova una gara con il robot da minisumo DarkBlade, chi l'avrà vinta?

{% include video id="3-lcMTfhhL0" provider="youtube" %}