---
title: "Ottobot"
excerpt: "(:it: in Italian) Exploration robot, base with Microchip dsPIC"
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2007
header:
  teaser: /assets/robot/ottobot/ottobot.jpg
  overlay_image: /assets/robot/ottobot/ottobot_header.jpg
---

Per il meccanismo di locomozione si sono, a suo tempo, scelte due ruote azionate da motori e un ruotino tale da permettere la stabilità sul piano. Tale sistema di locomozione, denominato “differential drive”, permette al robot di potersi muovere sul piano e di poter ruotare con facilità su se stesso, dando alla piattaforma mobilità nell’evitare ostacoli senza bisogno di manovre complesse (in figura la prima versione).

La scelta del tipo di ruote e la loro configurazione in un robot mobile vincola la navigazione dello stesso a uno specifico ambiente. Ad esempio il concorso DARPA dove le piattaforme mobili, automobili automatizzate, devono attraversare un deserto, la scelta di una configurazione “car-like” implicava dei movimenti per evitare ostacoli più complessi rispetto quelli che possono essere affrontati con una configurazione “unicycle-like”.

La prima versione del telaio è stata progettata nel 2007 ed era costituita da due motoridotti con due ruote con pneumatici, poste sull’asse di rotazione di ciascuno di essi; la terza ruota, il ruotino addizionale, era del tipo “caster wheel”. Le due ruote motorizzate erano poste sull’asse di simmetria del telaio, dalla forma di un ottagono dal diametro di 20cm, mentre il ruotino era posto ortogonalmente alle due ruote. Il ruotino era costituito da una ruota dalle dimensioni di 4cm montata su di un asse rigido, anch’esso di 4cm rotante intorno a un punto fisso sul telaio.

Tale ruotino però presentava l’inconveniente che, per particolari movimenti del robot, poteva porsi sullo stesso asse delle ruote motrici creando problemi di stabilità nei movimenti per la piattaforma mobile.

Sul telaio erano montate più schede elettroniche, una per il controllo controllo del robot chiamata “Motion Control”, costituita da una unico microcontrollore che esegue le funzioni di controllo, quelle di comunicazione e altre. La scheda aveva la possibilità di ricevere i segnali provenienti dagli encoder montati sugli assi dei motori e leggere la corrente da essi assorbita; era anche montata, in via temporanea, una scheda di comunicazione che permetteva di poter inviare i dati telemetrici al computer e poter controllare il robot.

Oltre alla scheda di controllo erano presenti le schede che permettevano la gestione dell’alimentazione dei motori e le schede di regolazione di potenza, quali il ponte-H pilotato dalla scheda di controllo tramite segnali PWM.

Il peso complessivo del robot era dovuto, in gran parte alle batterie al litio poste nella parte inferiore del telaio, al ruotino in acciaio e a parte dei supporti in ferro presenti nel telaio. Questo peso era causa della deformazione dei pneumatici delle ruote e quindi la stima della posizione del robot non era sufficientemente.

Questa prima versione non aveva sensori che permettessero di individuare ostacoli presenti nell’ambiente; è stato quindi necessario progettare una nuova versione utilizzando la medesima struttura, aggiungendo sensori di navigazione.

# Versione dotata di sensori

La nuova versione della piattaforma mobile è stata realizzata nel 2009 con la progettazione della scheda per l’acquisizione dei segnali provenienti dai sensori ambientali. Tale scheda era basata anch’essa su un microcontrollore che poteva processare i segnali, generare strategie di controllo avanzate, inviare i dati telemetrici e comandare la scheda “Motion Control”. Con questa nuova piattaforma il robot poteva navigare in ambienti strutturati.

La nuova scheda elettronica, chiamata “Navigation board”, poteva acquisire simultaneamente da otto sensori infrarossi analogici ed era predisposta per poter ricevere i segnali anche da altri sensori quali ad esempio quelli ultrasonici. Erano presenti più bus di comunicazione tra i quali il protocollo I2C, SPI, e più porte seriali per poter comunicare con possibili altri moduli. Sulla scheda erano montati anche sensori di corrente e tensione per poter quindi adottare strategie sulla gestione dell’alimentazione. La presenza di un sensore per la misura della temperatura rappresentava un elemento di correzione di misure soggette ad errori di deriva termica, quali ad esempio dei sensori ad ultrasuoni.

Per provare la nuova scheda venne costruito un primo telaio prototipo per verificare la corretta la disposizione dei sensori, messi al bordo del telaio ed affiancati tra loro nella parte frontale del robot in modo da diminuire le zone cieche, che non permettevano al robot di vedere gli ostacoli in quanto i sensori scelti possedevano un angolo di visione molto stretto (in figura la prima disposizione dei sensori). I sensori erano fissati con viti di metallo su distanziali anch’essi metallici. Furono aggiunti anche dei “parafanghi” sulle ruote per poter montarvici dei sensori. Altri due sensori che erano posti nella parte posteriore del robot per poter individuare altri possibili ostacoli.

Una volta scelta la disposizione dei sensori, fu deciso di montare i sensori nel telaio definitivo e poter quindi usare il sistema di visione per poter testare le prime leggi di controllo. In figura è presente un confronto tra la prima versione del telaio e la sua evoluzione sensorizzata.

La versione definitiva del telaio includeva anche un sistema di sensori di contatto per la rilevazione di ostacoli al contatto. Questo sistema era costituito da un pannello di alluminio serrato su di una cerniera, che, tramite un sistema di molle, assicurava la cedevolezza del sistema all’urto con un ostacolo e allo stesso tempo, tramite un interruttore, permetteva di inviare un segnale alla scheda di controllo per poter fermare il robot e attuare altre strategie di controllo per evitare che la piattaforma mobile urtasse oggetti incontrati nel suo percorso.



Durante i test fu notato l’assemblaggio dei sensori di contatto e di tutti i distanziali montati sulla struttura influiva negativamente sul peso del robot, accentuando l’effetto negativo sui pneumatici delle ruote; il peso complessivo del robot aveva raggiunto approssimativamente i 1.5 Kg e causava anche la deformazione dei sostegni di supporto dei motori rendendo ancora meno precise la stima delle coordinate della posizione del robot, essendo la variazione dell’interasse e il raggio della ruota parametri fondamentali per tale stima.

Inoltre l’altezza dei sensori, risultava di 10cm dal suolo, non permetteva al robot di vedere ostacoli più bassi e le vibrazioni provenienti dai motori e dal suolo causavano lo svitamento spontaneo delle viti di sostegno dei sensori, creando difficoltà nella percezione degli ostacoli.