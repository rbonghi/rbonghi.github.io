---
title: "Explorer"
excerpt: "(:it: in Italian) A simple exploration robot"
toc: true
toc_label: "Tavola dei contenuti"
toc_icon: "cog"
toc_sticky: true
number: 2011
header:
  teaser: /assets/robot/explorer/explorer.jpg
  overlay_image: /assets/robot/explorer/explorer_header.jpg
explorer:
  - url: /assets/robot/explorer/explorer-rendering.jpg
    image_path: /assets/robot/explorer/explorer-rendering.jpg
    alt: "Primo rendering del robot Explorer"
    title: "Primo rendering del robot Explorer"
  - url: /assets/robot/explorer/explorer-components.jpg
    image_path: /assets/robot/explorer/explorer-components.jpg
    alt: "Componenti del robot Explorer"
    title: "Componenti del robot Explorer"
  - url: /assets/robot/explorer/explorer-rendering-cover.jpg
    image_path: /assets/robot/explorer/explorer-rendering-cover.jpg
    alt: "Primo rendering del robot Explorer - Cover"
    title: "Primo rendering del robot Explorer- Cover"
  - url: /assets/robot/explorer/explorer-rendering-front.png
    image_path: /assets/robot/explorer/explorer-rendering-front.png
    alt: "Primo rendering del robot Explorer - Front"
    title: "Primo rendering del robot Explorer- Front"
  - url: /assets/robot/explorer/explorer-rendering-side.png
    image_path: /assets/robot/explorer/explorer-rendering-side.png
    alt: "Primo rendering del robot Explorer - Side"
    title: "Primo rendering del robot Explorer- Side"
  - url: /assets/robot/explorer/explorer-rendering-ultrasonic.jpg
    image_path: /assets/robot/explorer/explorer-rendering-ultrasonic.jpg
    alt: "Primo rendering del robot Explorer - Ultrasonic"
    title: "Primo rendering del robot Explorer- Ultrasonic"
box:
  - url: /assets/robot/explorer/explorer-box-01.jpg
    image_path: /assets/robot/explorer/explorer-box-01.jpg
    alt: "Assi colorate per Explorer"
    title: "Assi colorate per Explorer"
  - url: /assets/robot/explorer/explorer-box-02.jpg
    image_path: /assets/robot/explorer/explorer-box-02.jpg
    alt: "Scatola ultimata"
    title: "Scatola ultimata"
  - url: /assets/robot/explorer/explorer-box-03.jpg
    image_path: /assets/robot/explorer/explorer-box-03.jpg
    alt: "Pannelli in gomma"
    title: "Pannelli in gomma"
  - url: /assets/robot/explorer/explorer-box-04.jpg
    image_path: /assets/robot/explorer/explorer-box-04.jpg
    alt: "Disposizione robot"
    title: "Disposizione robot"
  - url: /assets/robot/explorer/explorer-box-05.jpg
    image_path: /assets/robot/explorer/explorer-box-05.jpg
    alt: "Disposizione robot alto"
    title: "Disposizione robot alto"
  - url: /assets/robot/explorer/explorer-box-06.jpg
    image_path: /assets/robot/explorer/explorer-box-06.jpg
    alt: "Robot e scatola"
    title: "Robot e scatola"
---

Sulla base delle esperienze del robot [Ottobot](/robot/ottobot) e tenendo conto delle imperfezioni delle precedenti versioni del telaio è stato sviluppato uno nuovo telaio che potesse risolvere tutti
quei difetti che erano man mano apparsi, come il peso complessivo del robot e il difficile serraggio delle viti dei sensori infrarossi. Si iniziò quindi la progettazione del nuovo telaio usando un programma CAD di disegno meccanico (Solidworks) con i risultati visibili nelle figure successive.

Prima di tutto sono state cambiate le ruote e il ruotino. Le nuove ruote non avevano una camera d'aria ma una gomma rigida tale da assicurare un buona tenuta sul terreno, eliminando allo stesso tempo, possibili deformazioni dovute al peso. Il ruotino è stato sostituito con una "omniwheel" dando al robot la possibilità di poter, comunque, ruotare sul piano senza che la ruota si allineasse con le ruote motrici.

# Telaio

Il telaio è stato totalmente riprogettato definendo un sistema di piani modulari, su ciascuno di dei quali erano montati i vari componenti meccanici ed elettronici, i vari sensori erano incastrati e avvitati sulle pareti, aumentando così la solidità della struttura.

Sul primo livello, un piano di 6mm di PVC espanso di forma dodecagonale, erano montati i motori e il ruotino, con uno spazio per le batterie. Su questo piano erano presenti anche le schede di potenza, quali quelle di alimentazione e di controllo motori, vedi in figura successiva. Su questo livello erano anche stati predisposti un insieme di fori per poter aggiungere ulteriori sensori e/o componenti aggiuntivi, uno scasso frontale per la possibile aggiunta di sensori per il riconoscimento di linee sul pavimento e quattro fori per l'eventuale montaggio di un paraurti frontale onde evitare dannosi urti del robot con ostacoli.

{% include gallery id="explorer" caption="Rendering e parti di Explorer" %}

Tra un livello e l'altro sono stati disposti sul bordo, dodici pannelli da 2mm di Poliver (materiale simile al Plexyglass), su sette dei quali sono stati incassati e avvitati con viti in nylon i sensori infrarossi; su un altro pannello sono stati montati tutta la pulsantiera e i jack di alimentazione per accendere o ricaricare il robot.

Con questa nuova configurazione l'altezza complessiva dei sensori infrarossi è diventata di 7cm da terra, recuperando centimetri utili per vedere ostacoli posti ad altezze più basse.

Il design del nuovo telaio in PVC espanso e Poliver, costituito da elementi dodecagonali per quanto riguarda i piani, e i pannelli laterali, entrambi senza angoli smussati (in figura i vari pannelli) assicurano il basso costo nella produzione del telaio con macchine CNC dando, allo stesso tempo, grande solidità alla struttura.


Sul secondo piano anch'esso PVC espanso tagliato in forma dodecagonale, sono state montate tutte le varie schede di controllo del robot, "Motion Control", "Navigation board" e la scheda di comunicazione. I vari piani sono fissati mediante un sistema di viti filettate e colonne in carbonio, tale sistema assicura maggiore resistenza agli urti involontari del robot, garantendo un peso minore rispetto a sistemi costituiti da colonne in ottone o acciaio.

Una volta assemblato, il nuovo telaio della piattaforma mobile (in figura) grazie al sistema di pannelli, fa si che i sensori sono disposti con maggiore solidità e sono collocati con maggiore simmetria all'interno della struttura. La scelta di rimuovere i sensori di contatto frontali ha permesso di ridurre il peso del robot complessivamente di 500g e con il sistema di colonne per il montaggio dei vari livelli si è assicurata la possibilità di aggiungere facilmente nuovi piani alla piattaforma mobile per l'aggiunta di nuova componentistica: i sensori ultrasonici, telecamere ed altro (una seconda figura frontale del robot).

{% include figure image_path="/assets/robot/explorer/explorer-building.jpg" alt="Explorer costruzione" caption="Explorer costruzione" %}

La scelta della "omniwheel" al posto della "caster wheel" assicura alla piattaforma mobile maggiore stabilità statica senza comprometterne la facilità nei movimenti.

Il nome scelto per questo robot è "Explorer", ed è concepito per l'esplorazione in ambienti strutturati, quali ad esempio labirinti o simulazioni di ambienti complessi. Grazie alla costruzione del nuovo telaio e alla sua progettazione mediante CAD è stato possibile progettare il telaio affinché sia possibile produrlo in serie, senza che questo influisca sui costi.

## Livello motori

{% include figure image_path="/assets/robot/explorer/explorer-groundFrame.jpg" alt="Explorer Livello motori" caption="Explorer Livello motori" %}

Nel primo livello sono disposti i due motori con encoder. In questa sezione è stato ricavato lo spazio per poter mettere le batterie (non presenti nella foto) il ruotino omnidirezionale posto posteriormente, ed infine tutta l’elettronica di potenza che gestisce l’alimentazione del robot sia per quanto riguarda i motori con il [ponte-H](/project/h-bridge) e per quanto riguarda la distribuzione dell’energia alle schede di controllo e sensori, la [Reg-Board](/project/regboard). Sulle pareti del primo piano sono disposti i sette sensori infrarossi per poter riconoscere ostacoli nelle brevi distanze.

## Livello sensori

{% include figure image_path="/assets/robot/explorer/explorerLivello1.jpg" alt="Explorer Livello sensori" caption="Explorer Livello sensori" %}

Nel secondo livello sono disposti le schede di controllo dei motori quale la [Motion Control](/project/motion-control), la scheda di controllo e acquisizione dati, la [Navigation Board](/project/navigation-board), proveniente da tutti i sensori quali quelli infrarossi e quelli ultrasuoni posti sulle pareti del robot.
Infine sono montati sui pannelli laterali anche i pannelli di supporto per poter collegare l’ICD3 (Microchip In Circuit Debugger) e riprogrammare i controllori presenti sulle schede logiche. Le schede di comunicazione sono collegati alla scheda di controllo di alto livello tramite un convertitore seriale-USB.

## Livello controllo

{% include figure image_path="/assets/robot/explorer/explorer-Livello2.jpg" alt="Explorer Livello controllo" caption="Explorer Livello controllo" %}

Nell’ultimo livello è presente la Beaglebone Black una scheda con linux a bordo, tale scheda permette di comunicare e gestire le schede di basso livello e governare il robot. Il sistema di sviluppo posto sul robot è ROS. Affinché la scheda sia alimentata è presente anche un piccolo regolatore di tensione che porta la tensione proveniente dalla Reg-Board alla tensione richiesta.

## Jetson TK1

{% include figure image_path="/assets/robot/explorer/explorer-Jetson-LOW.png" alt="Explorer con NVIDIA Jetson TK1" caption="Explorer con NVIDIA Jetson TK1" %}

Questa versione è stato un test di utilizzo del robot Explorer usando una NVIDIA Jetson TK1, sulla base di questo test si è passati a [Dude](/robot/dude)

# Box

Dopo aver progettato il robot Explorer si è reso necessario costruire un box capace a portare il robot con comodità al di fuori dell’ambiente domestico evitando che urti,  intemperie o polvere potessero rovinare il robot al suo interno.

Si è scelto quindi di progettare la borsa partendo da una struttura in legno multi strato da 1cm, dalle dimensioni di 35cm x 24cm x 25cm. Come visibile dall’immagine seguente la scatola è stata colorata con la medesima livrea del robot, giallo ed un bordo nero.

Una volta assemblata la scatola è stata dotata di una maniglia di trasporto montata sul coperchio superiore e due cerniere frontali tali da poter chiudere assicurandone il trasporto con facilità. Inoltra lateralmente sono stati installati dei supporti in metallo tali da poter essere montata una tracolla.

Per assicurare che all’interno il robot non subisse urti con la scatola sono stati inseriti dei pannelli in gomma piuma rivestiti di stoffa gialla tali da mantenere il robot fisso ma capaci di assorbire gli urti e le vibrazioni durante il trasporto.

La scatola è stata dotata di un secondo coperchio capace di assicurare la facilità di presa del robot durante le fasi di inserimento ed estrazione. E stato lasciato lateralmente un cassetto per poter portare altri componenti utili al robot, quali carica batterie, elementi di sostituzione o manuali di controllo.

Nelle immagini seguenti si possono osservare i vani della scatola ed i pannelli in gomma piuma. Il vano dove è possibile portare il robot ha uno spazio utile (contando anche lo spazio occupato dalla gomma piuma) di 21cm x 21cm x 21 cm, mentre il vano laterale di 23cm x 10cm x 23cm.

{% include gallery id="box" caption="Costruzione del box di trasporto" %}

# Telemetria

{% include figure image_path="/assets/robot/explorer/explorer-plotter.jpg" alt="Explorer plotter" caption="Explorer plotter" %}

Con lo sviluppo del nuovo robot si rese necessario riprogettare il sistema di telemetria di [Ottobot](/robot/ottobot), durante la progettazione si tenne conto dei vari elementi di controllo e la necessità di poter controllare e modificare i vari parametri del robot. Si iniziò quindi a delineare il disegno del nuovo programma “Plotter” che iniziava a garantire le prime specifiche di controllo (nella figura affianco).

Si iniziò ad implementare una prima versione di simulatore che permetteva di pilotare il robot disegnato nel programma e testare le leggi di controllo, ma la difficoltà di implementare nuovi comandi come quella di dover riprogettare le schermate di controllo comportò una nuova riprogettazione del sistema complessivo.

Dall’esperienza acquisita nella realizzazione dei software precedenti si iniziò a progettare una nuova IDE (Integrated Development Environment) capace di garantire la facilità negli aggiornamenti dal punto di realizzativo e con la capacità di integrare un sistema di simulazione di robot mobili generando quindi ostacoli virtuali e permettere a robot virtuali e reali di poter evitarli, simulando così leggi di controllo avanzate.

L’IDE di sviluppo è costituita da elementi mobili, nella figura successiva, quali la mappa dinamica dei robot ed un grafico istantaneo per valutare visivamente delle variabili della piattaforma mobile, il programma permette di poter avere più informazioni in contemporanea dal robot e poter salvare i dati ricevuti o simulati dal programma in un formato che sia leggibile da altri programmi quali ad esempio “Matlab” dando quindi la possibilità all’utilizzatore di poter sviluppare e valutare le leggi di controllo su software di calcolo computazionale più precisi.

{% include figure image_path="/assets/robot/explorer/explorer-programma02.jpg" alt="Explorer GUI 1" caption="Explorer GUI 1" %}

Nella IDE si possono simulare in contemporanea più robot mobili ed è possibile inserire in maniera dinamica più ostacoli per poter costruire un ambiente di simulazione utile per gli studi. Sulla sinistra della schermata è possibile visionare tutti i robot presenti ed è possibile impostare in tempo reale i metodi di comunicazione del robot con l’esterno. Questo permette di poter simulare il comportamento del robot e quando necessario iniziare a ricevere i dati dal robot reale senza cambiare programma.

É possibile pilotare manualmente il robot per poter verificare il corretto funzionamento del robot e nella mappa principale del programma è possibile impostare una direzione di moto da far raggiungere al robot, potendo vedere in contemporanea il percorso dal robot eseguito.

La IDE di sviluppo è sviluppata anche in maniera tale da garantire uno sviluppo graduale delle sue parti, senza intaccare il resto del codice presente. Questa scelta è divenuta di grande utilità, vista la facilità di sviluppare nuovi sistemi di controllo o nuove componenti per la piattaforma mobile. Si è tenuto conto anche della possibilità di pilotare più robot con diversi protocolli di comunicazione oltre quello ZigBee trattato precedentemente. Infatti è possibile poter comunicare con altri robot anche con protocolli di rete WI-FI o direttamente andando ad usare la porta seriale.

## Robot builder

É stato sviluppato in dettaglio un sistema di costruzione del robot, all’interno del programma di sviluppo dando quindi la possibilità all’utilizzatore di poter configurare in poco tempo i parametri necessari per farlo funzionare. Nella schermata, nella figura successiva, si possono vedere le varie componenti disponibili nella “palette” ed i componenti che un robot nell’esempio è dotato.

{% include figure image_path="/assets/robot/explorer/explorer-programma03.jpg" alt="Explorer GUI 2" caption="Explorer GUI 2" %}

Si possono integrare molti componenti, da componenti meccaniche o di controllo, quali:
* Struttura del robot;
* Ruote;
* PID;
* Controlli di alto livello;
* Sistemi di guida manuale;
* Sensori infrarossi, ultrasuoni, etc etc;
* Variabili aggiuntive di controllo.

Una volta ultimata la “costruzione” del progetto, questo viene automaticamente salvato in una cartella dove al suo interno sono contenute tutte le varie configurazioni del robot e tutte gli archivi di dati salvati durante le varie simulazioni.

{% include figure image_path="/assets/robot/explorer/explorer-programma04.jpg" alt="Explorer GUI 3" caption="Explorer GUI 3" %}

É sempre possibile aggiornare il progetto del robot in ogni suo momento e configurare con facilità i vari parametri del robot, come è possibile vedere nella schermata successiva relativa ai vari parametri di gestione.

## Simulatore

La IDE ha al suo interno un sistema di simulazione che garantisce una simulazione dei vari componenti presenti e simula il comportamento dei sensori in presenza di ostacoli, una libreria di gestione di poligoni restituisce il valore generato dai sensori virtuali ed invia il valore letto al robot relativo, quale che sia virtuale o reale.

{% include figure image_path="/assets/robot/explorer/explorer-programma05.jpg" alt="Explorer GUI 4" caption="Explorer GUI 4" %}

Com’è possibile vedere dall’ultima schermata sono stati simulati più di un robot ed alcuni di essi hanno riconosciuto l’ostacolo (il cubo nero) presente in traiettoria, garantendo quindi la possibilità di far adottare strategie di controllo tali da evitare l’ostacolo e come verranno trattate nel capitolo successivo.

## Codici

Il codice del framework di controllo del robot è disponibile su Github al seguente indirizzo:

[RBFramework](https://github.com/rbonghi/RBFramework.git) ed i file di esempio: [World-RBFramework](https://github.com/rbonghi/World-RBFramework.git)

# Controllo su ROS

{% include video id="gGOCGs0BvcA" provider="youtube" %}
