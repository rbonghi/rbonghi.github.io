---
title: "Ottobot"
excerpt: "(:it: in Italian) Exploration robot, base with Microchip dsPIC"
toc: true
toc_label: "Tavola dei contenuti"
toc_icon: "cog"
toc_sticky: true
number: 2007
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  teaser: /assets/robot/ottobot/ottobot.jpg
  overlay_image: /assets/robot/ottobot/ottobot_header.jpg
first-version:
  - url: /assets/robot/ottobot/ottobot-firstChassis.jpg
    image_path: /assets/robot/ottobot/ottobot-firstChassis.jpg
    alt: "Prima versione Ottobot - Top"
    title: "Prima versione Ottobot - Top"
  - url: /assets/robot/ottobot/ottobot-firstChassisBottom.jpg
    image_path: /assets/robot/ottobot/ottobot-firstChassisBottom.jpg
    alt: "Prima versione Ottobot - Vista inferiore"
    title: "Prima versione Ottobot - Vista inferiore"
sensors:
  - url: /assets/robot/ottobot/ottobot-sensorPositioning.jpg
    image_path: /assets/robot/ottobot/ottobot-sensorPositioning.jpg
    alt: "Sensori Ottobot"
    title: "Sensori Ottobot"
  - url: /assets/robot/ottobot/ottobot-twoChassis.jpg
    image_path: /assets/robot/ottobot/ottobot-twoChassis.jpg
    alt: "Confronto telai"
    title: "Confronto telai"
second-version:
  - url: /assets/robot/ottobot/ottobot.jpg
    image_path: /assets/robot/ottobot/ottobot.jpg
    alt: "Seconda versione"
    title: "Seconda versione"
  - url: /assets/robot/ottobot/ottobot-secondChassisFrontal.jpg
    image_path: /assets/robot/ottobot/ottobot-secondChassisFrontal.jpg
    alt: "Seconda versione, vista frontale"
    title: "Seconda versione, vista frontale"
  - url: /assets/robot/ottobot/ottobot-secondChassisHigh.jpg
    image_path: /assets/robot/ottobot/ottobot-secondChassisHigh.jpg
    alt: "Seconda versione, vista dall'alto"
    title: "Seconda versione, vista dall'alto"
floors:
  - url: /assets/robot/ottobot/ottobot-robotalto.jpg
    image_path: /assets/robot/ottobot/ottobot-robotalto.jpg
    alt: "Ottobot"
    title: "Ottobot"
  - url: /assets/robot/ottobot/ottobot-strutturarobot2.jpg
    image_path: /assets/robot/ottobot/ottobot-strutturarobot2.jpg
    alt: "Ottobot vista livelli"
    title: "Ottobot vista livelli"
telemetry:
  - url: /assets/robot/ottobot/ottobot-miniplotter.jpg
    image_path: /assets/robot/ottobot/ottobot-miniplotter.jpg
    alt: "Ottobot telemetria"
    title: "Ottobot telemetria"
  - url: /assets/robot/ottobot/ottobot-miniplotter2.png
    image_path: /assets/robot/ottobot/ottobot-miniplotter2.png
    alt: "Ottobot telemetria con sensori"
    title: "Ottobot telemetria con sensori"
---

Per il meccanismo di locomozione si sono, a suo tempo, scelte due ruote azionate da motori e un ruotino tale da permettere la stabilità sul piano. Tale sistema di locomozione, denominato “differential drive”, permette al robot di potersi muovere sul piano e di poter ruotare con facilità su se stesso, dando alla piattaforma mobilità nell’evitare ostacoli senza bisogno di manovre complesse (in figura la prima versione).

La scelta del tipo di ruote e la loro configurazione in un robot mobile vincola la navigazione dello stesso a uno specifico ambiente. Ad esempio il concorso DARPA dove le piattaforme mobili, automobili automatizzate, devono attraversare un deserto, la scelta di una configurazione “car-like” implicava dei movimenti per evitare ostacoli più complessi rispetto quelli che possono essere affrontati con una configurazione “unicycle-like”.

La prima versione del telaio è stata progettata nel 2007 ed era costituita da due motoridotti con due ruote con pneumatici, poste sull’asse di rotazione di ciascuno di essi; la terza ruota, il ruotino addizionale, era del tipo “caster wheel”. Le due ruote motorizzate erano poste sull’asse di simmetria del telaio, dalla forma di un ottagono dal diametro di 20cm, mentre il ruotino era posto ortogonalmente alle due ruote. Il ruotino era costituito da una ruota dalle dimensioni di 4cm montata su di un asse rigido, anch’esso di 4cm rotante intorno a un punto fisso sul telaio.

Tale ruotino però presentava l’inconveniente che, per particolari movimenti del robot, poteva porsi sullo stesso asse delle ruote motrici creando problemi di stabilità nei movimenti per la piattaforma mobile.

Sul telaio erano montate più schede elettroniche, una per il controllo controllo del robot chiamata “Motion Control”, costituita da una unico microcontrollore che esegue le funzioni di controllo, quelle di comunicazione e altre. La scheda aveva la possibilità di ricevere i segnali provenienti dagli encoder montati sugli assi dei motori e leggere la corrente da essi assorbita; era anche montata, in via temporanea, una scheda di comunicazione che permetteva di poter inviare i dati telemetrici al computer e poter controllare il robot.

Oltre alla scheda di controllo erano presenti le schede che permettevano la gestione dell’alimentazione dei motori e le schede di regolazione di potenza, quali il ponte-H pilotato dalla scheda di controllo tramite segnali PWM.

Il peso complessivo del robot era dovuto, in gran parte alle batterie al litio poste nella parte inferiore del telaio, al ruotino in acciaio e a parte dei supporti in ferro presenti nel telaio. Questo peso era causa della deformazione dei pneumatici delle ruote e quindi la stima della posizione del robot non era sufficientemente.

{% include gallery id="first-version" caption="Prima versione Ottobot" %}

Questa prima versione non aveva sensori che permettessero di individuare ostacoli presenti nell’ambiente; è stato quindi necessario progettare una nuova versione utilizzando la medesima struttura, aggiungendo sensori di navigazione.

# Versione dotata di sensori

La nuova versione della piattaforma mobile è stata realizzata nel 2009 con la progettazione della scheda per l’acquisizione dei segnali provenienti dai sensori ambientali. Tale scheda era basata anch’essa su un microcontrollore che poteva processare i segnali, generare strategie di controllo avanzate, inviare i dati telemetrici e comandare la scheda “Motion Control”. Con questa nuova piattaforma il robot poteva navigare in ambienti strutturati.

La nuova scheda elettronica, chiamata “Navigation board”, poteva acquisire simultaneamente da otto sensori infrarossi analogici ed era predisposta per poter ricevere i segnali anche da altri sensori quali ad esempio quelli ultrasonici. Erano presenti più bus di comunicazione tra i quali il protocollo I2C, SPI, e più porte seriali per poter comunicare con possibili altri moduli. Sulla scheda erano montati anche sensori di corrente e tensione per poter quindi adottare strategie sulla gestione dell’alimentazione. La presenza di un sensore per la misura della temperatura rappresentava un elemento di correzione di misure soggette ad errori di deriva termica, quali ad esempio dei sensori ad ultrasuoni.

Per provare la nuova scheda venne costruito un primo telaio prototipo per verificare la corretta la disposizione dei sensori, messi al bordo del telaio ed affiancati tra loro nella parte frontale del robot in modo da diminuire le zone cieche, che non permettevano al robot di vedere gli ostacoli in quanto i sensori scelti possedevano un angolo di visione molto stretto (in figura la prima disposizione dei sensori). I sensori erano fissati con viti di metallo su distanziali anch’essi metallici. Furono aggiunti anche dei “parafanghi” sulle ruote per poter montarvici dei sensori. Altri due sensori che erano posti nella parte posteriore del robot per poter individuare altri possibili ostacoli.

{% include gallery id="sensors" caption="Sensori" %}

Una volta scelta la disposizione dei sensori, fu deciso di montare i sensori nel telaio definitivo e poter quindi usare il sistema di visione per poter testare le prime leggi di controllo. In figura è presente un confronto tra la prima versione del telaio e la sua evoluzione sensorizzata.

# Seconda versione

La versione definitiva del telaio includeva anche un sistema di sensori di contatto per la rilevazione di ostacoli al contatto. Questo sistema era costituito da un pannello di alluminio serrato su di una cerniera, che, tramite un sistema di molle, assicurava la cedevolezza del sistema all’urto con un ostacolo e allo stesso tempo, tramite un interruttore, permetteva di inviare un segnale alla scheda di controllo per poter fermare il robot e attuare altre strategie di controllo per evitare che la piattaforma mobile urtasse oggetti incontrati nel suo percorso.

{% include gallery id="second-version" caption="Seconda versione" %}

Durante i test fu notato l’assemblaggio dei sensori di contatto e di tutti i distanziali montati sulla struttura influiva negativamente sul peso del robot, accentuando l’effetto negativo sui pneumatici delle ruote; il peso complessivo del robot aveva raggiunto approssimativamente i 1.5 Kg e causava anche la deformazione dei sostegni di supporto dei motori rendendo ancora meno precise la stima delle coordinate della posizione del robot, essendo la variazione dell’interasse e il raggio della ruota parametri fondamentali per tale stima.

Inoltre l’altezza dei sensori, risultava di 10cm dal suolo, non permetteva al robot di vedere ostacoli più bassi e le vibrazioni provenienti dai motori e dal suolo causavano lo svitamento spontaneo delle viti di sostegno dei sensori, creando difficoltà nella percezione degli ostacoli.

# Architettura

Affinché il robot Ottobot possa ricevere le coordinate di destinazione, in modo tale da giungere alla destinazione desiderata. Queste operazioni sono gestite dalla comunicazione della scheda [Navigation Board](/project/navigation-board) e la [Motion control](/project/motion-control).

{% include figure image_path="/assets/robot/ottobot/ottobot-collegamenti.jpg" alt="Ottobot architettura" caption="Ottobot architettura" %}

La comunicazione tra le due schede avviene tramite protocollo SPI, che permette di condividere le informazioni della memoria tra entrambe le schede. La navigation board ed il modulo radio XBee la comunicazione tramite protocollo seriale.

L'alimentazione giunge dalle batterie e viene distribuita, una volta regolata dalla Reg-Board alle varie schede, mentre giunge direttamente ai motori attraverso l'H-bridge.
La figura precedente rimane esplicativa sull'architettura generale del robot.

## Task manager

Affinché tutte le operazioni di controllo e pianificazione del robot possano funzionare al meglio, è stato implementato uno scheduler sul microcontrollore che permette di pianificare le varie operazioni da eseguire nell'intervallo disponibile dalla CPU del microcontrollore.

{% include figure image_path="/assets/robot/ottobot/ottobot-roundrobing.jpg" alt="Ottobot task manager" caption="Ottobot task manager" %}

Le funzioni sono schedulate in ordine di priorità:

1. Elaborazione PID
2. Calcolo odometria
3. Elaborazione Regolazione cartesiana
4. Invio dati su porta seriale

{% include figure image_path="/assets/robot/ottobot/ottobot-scheduler.png" alt="Ottobot scheduler" caption="Ottobot scheduler" %}

In contemporanea a queste operazioni schedulate, il microcontrollore deve gestire delle interruzioni sincrone ed asincrone che vengono inviate dalle varie periferiche interne del microcontrollore. Gli interrupt provenienti dalle periferiche sono:

* DMA0 - Trasmissione seriale - **asincrona**
* DMA1 - Acquisizione ADC - **sincrona** ogni 100ms
* InputCapture 1 - **asincrona**
* InputCapture 2 - **asincrona**
* Timer 1 - Timer di sistema -  **sincrona** ogni 1ms
* Timer 2 - Timer PWM - **sincrona** ogni Xms
* Acquisizione seriale - **asincrona**

## Comunicazione

Il sistema principale che il robot utilizza per trasmettere la telemetria e ricevere i comandi di controllo e di gestione è composto da due sotto-sistemi: una macchina a stati finiti (nella figura successiva) che gestisce il pacchetto ricevuto ed un interprete che esegue l’operazione richiesta.

{% include figure image_path="/assets/robot/ottobot/ottobot-asfuart.jpg" alt="Ottobot comunicazione" caption="Ottobot comunicazione" %}

La struttura del pacchetto è definita nel modo seguente:
```
|1| 2 |  3  |4...     N-1|  N  |
|#|CMD| LNG |dati...  ...| CKS |
```

* Header del messaggio
* Comando di controllo
* LNG = Numero di dati contenuti nel pacchetto
* Dati del messaggio
* Contenuto del messaggio
* N. CeckSum di chiusura

Una volta verificata la corretta ricezione del pacchetto per mezzo del checksum posto alla fine del pacchetto, il messaggio decodificato viene inviato ad un interprete che esegue l’ordine ricevuto.

# I livelli

Il robot Ottobot è di tipologia uniciclo, il telaio dalla forma ottagonale, su cui sono stati montati i motori, batterie e tutta l'elettronica di controllo. Questo è dotato di 2 motori DC pilotati da un ponte H di potenza. Per l'alimentazione è presente una scheda dedicata, dotata di regolatore DC-DC switching. L'intera logica di controllo è gestita dall'unità centrale chiamata “Motion control”.

{% include gallery id="floors" caption="Livelli" %}

La struttura del robot è possibile distinguere due livelli, uno di potenza, ed un secondo di controllo. La struttura compatta, dimensione massima di (20cm) garantisce al robot di poter passare in piccoli pertugi.

## Livello 0

Dedicato all'allogiamento motori e delle schede di potenza del robot, si possono distinguere chiaramente i due motori su cui sono montati direttamente sull'asse della riduzione le due ruote, in basso il ruotino (terzo punto di appoggio del robot) e due piccoli supporti per tenere le batterie del robot.

{% include figure image_path="/assets/robot/ottobot/ottobot-firstChassisBottom.jpg" alt="Ottobot livello 0" caption="Ottobot livello 0" %}

## Livello 1

Su questo piano, dedicato alla logica di controllo è presente la scheda che pilota i motori, comunica la telemetria (posizione, stato motori, velocità, etc etc) al pc. La comunicazione è garantita dal modulo radio XBee.

{% include figure image_path="/assets/robot/ottobot/ottobot.jpg" alt="Ottobot livello 1" caption="Ottobot livello 1" %}

Il livello 1 è stato aggiornato, al fine di dare la possibilità al robot di superare ostacoli, cosa che precedentemente non era possibile. Sono stati quindi aggiunti sei sensori infrarossi per coprire i 180° gradi frontali del robot e due sensori infrarossi posti posteriormente al robot, infine sono stati aggiunti tre bumper frontali, per rilevare contatti frontali con ostacoli.

# Telemetria

La gestione e l’analisi del comportamento del robot viene eseguito dal software MiniPlotter, un programma che permette di visionare in real time l’andamento del robot, di gestirne il movimento e di inviare le coordinate per la regolazione cartesiana. Il sistema è stato sviluppato in Java, per consentire una facile portabilitá da un sistema operativo ad un altro.

Questa applicazione è costituita da un area sulla sinistra dove è possibile leggere direttamente i pacchetti ricevuti dal robot, subito sotto c'è la possibilità di scrivere a mano i pacchetti attraverso un piccolo prompt di comandi.  L'area posta al di sotto, costituita da un insieme di pulsanti e campi di testo, garantiscono all'utilizzatore la possibilità di pilotare sia manualmente (con comandi di velocità lineare e angolare) o inserendo le coordinate di arrivo.

{% include gallery id="telemetry" caption="Telemetria ottobot" %}

Infine l'area sulla destra rappresenta la mappa dove il robot vi navigherà. Su di esso è raffigurato il centro cinematico del robot (colorato di rosso) ed in blu la mappa dei punti degli ostacoli letti dai sensori del robot.

{% include figure image_path="/assets/robot/ottobot/ottobot-plotter-old.jpg" alt="Ottobot telemetria processing" caption="Ottobot telemetria processing" %}

Successivamente è stata sviluppata una nuova interfaccia usando il sistema di sviluppo [Processing](http://processing.org/), di guida del robot dove potesse essere più leggibile il posizionamento del robot nello spazio, attraverso due mappe una mini mappa con il posizionamento globale, ed una con la posizione locale del robot.