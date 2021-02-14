---
title: "H Bridge"
excerpt: "(:it: in Italian) It's a powerful H-Bridge with an L298. With this simple board the robot Ottobot and Explorer can control their DC motors. It was built in 2008 and with different tests to check the performance in robotics field."
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2008
header:
  teaser: /assets/project/h-bridge/H-Bridge2.jpg
---

Per poter controllare i motori si è reso necessario sviluppare una scheda che permettesse di pilotarli utilizzando i segnali provenienti dalla logica di controllo, adattati alle potenze richieste dal motore (nell’immagine è illustrato il rendering della scheda di controllo motori).

{% include figure image_path="/assets/project/h-bridge/H-Bridge-Front.jpg" alt="Rendering ponte" caption="Rendering ponte" %}

La scheda, denominata “H-Bridge” (nella figura successiva), agisce da adattatore di potenza e permette di muovere i motori in ambedue i sensi di rotazione. L “H-Bridge”, realizzato all’interno di un singolo circuito integrato, è costituito da quattro transistor che “agiscono da interruttori”. Il loro funzionamento è spiegato nel dettaglio nella pagina sui convertitori DC/DC ed i ponti-H.

{% include figure image_path="/assets/project/h-bridge/H-Bridge2.jpg" alt="Ponte H" caption="Ponte H" %}

Questa scheda costituisce il modulo di interfaccia tra la scheda di controllo ed i motori. I segnali in ingresso, solitamente PWM vengono “trasformati” in segnali di potenza utili a movimentare l’attuatore. Affinché questo sia possibile si utilizza il ponte-H L298, capace di gestire una corrente massima su motore di  4A.

Le caratteristiche salienti della scheda sono qui elencate:
* Doppio ponte-H con integrato L298;
* Corrente massima su motore DC 4A;
* Alimentazione 9-24V e regolatore interno per la logica del L298;
* Sensori per la lettura della corrente di carico sui motori;
* LED di controllo verso di rotazione;
* Disabilitazione “H-Bridge” attraverso il pin di “enable”;
* Dimensioni 45 55mm;
* Ripple della scheda nell’ordine dei 10mV;
* PWM consigliato.

{% include figure image_path="/assets/project/h-bridge/testHbridge.jpg" alt="Test Ponte H" caption="Test Ponte H" %}

Per poter verificare il perfetto funzionamento del motore e dell’H-Bridge, si è predisposto un sistema di test, i cui elementi sono mostrati nella figura precedente.

# Test

Misurando la tensione ai capi del motore, si è misurato il ripple presente in uscita dalla scheda di controllo (nella figura successiva) e la frequenza di PWM massima sopportabile dal sistema. Alla fine di tali test si sono quindi definiti i valori effettivamente utili per il sistema di controllo.

{% include figure image_path="/assets/project/h-bridge/HbridgeNonfiltrato1.jpg" alt="ripple spazzole" caption="ripple spazzole" %}

E' interessante osservare il ripple dovuto alla commutazione delle spazzole durante la rotazione, mostrato nella figura successiva, sono ad una frequenza troppo alta.

{% include figure image_path="/assets/project/h-bridge/HbridgeFiltrato.jpg" alt="Dopo filtro spazzole" caption="Dopo filtro spazzole" %}

Infine nell'ultima figura è visibile la temperatura raggiunta dalla scheda con i due motori attivi, si nota la temperatura di 45C raggiunta dall'integrato dopo 5 minuti di attività.

{% include figure image_path="/assets/project/h-bridge/Ponte1.jpg" alt="Misura temperatura" caption="Misura temperatura" %}