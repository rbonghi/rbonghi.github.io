---
title: "Navigation Board"
excerpt: "(:it: in Italian) With a Microchip dsPIC33 this board can receive different analog values simultaneously. With different filter and other information from the Motion control this board can control the robot with an obstacle avoidance."
permalink: /project/navigation-board/
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2008
header:
  teaser: /assets/project/navigation-board/navigationboard_0.jpg
---

La gestione il sistema di visione è stata sviluppata la scheda "Navigation board" che ha come integrato il dsPICFJ128GP804 questo microcontrollore ha al suo interno un DSP (Digital Signal Processing), questo è ottimizzato per una elaoborazione efficiente di segnali digitali e quindi anche segnali continui dopo essere stati campionati dal convertitore A/D.

{% include figure image_path="/assets/project/navigation-board/navigation-board-top.jpg" alt="Rendering navigation board" caption="Rendering navigation board" %}

In figura è rappresentato il primo rendering della scheda, dove è possibile vedere il gran numero di connettori che permettono di poter ricevere i dati dai vari sensori della piattaforma mobile ed al centro il microcontrollore.

{% include figure image_path="/assets/project/navigation-board/navigationboard_0.jpg" alt="Navigation board" caption="Navigation board" %}

Sono caratterizzate brevemente le caratteristiche principali della scheda:
* microcontrollore dsPIC33FJ128GP804;
* gestione di 8 sensori infrarossi;
* lettura della corrente e tensione delle batterie;
* 2 led di controllo;
* Bus I²C sia 3.3 volt che 5 volt;
* 2 Bus SPI;
* Comunicazion seriale;
* Gestione di 3 sensori di contatto;
* Possibilità di spegnere i sensori direttamente dalla scheda;
* Possibilità di scegliere una alimentazione separata per i sensori.

La scheda ha saldato un sensore di temperatura per poter misurare la temperatura ambientale e poter essere usato quindi come strumento di misura, mentre è predisposta per ricevere il segnale analogico proveniente dai sensori infrarossi, che come da specifiche necessitano di condensatori elettrolitici per la compensazione dei disturbi di tensione. I due connettori "molex" (i più grandi al di sotto della scheda) di cui è dotata la scheda garantiscono la connessione alla scheda "Motion control" ed alla scheda di comunicazione "XBee board".

{% include figure image_path="/assets/project/navigation-board/sensori.jpg" alt="Navigation board sensori" caption="Navigation board sensori" %}

La scheda una volta ultimata si presenta come nella figura precedente, le specifiche di questa scheda assicurano comunque un buon funzionamento all'interno della piattaforma mobile, il secondo regolatore di tensione che alimenta soltanto i sensori assicura la corretta erogazione di energia da parte dei regolatori di tensione presenti sulle schede e da la possibilità di controllare esternamente da una porta digitale del microcontrollore di abilitare l'erogazione della corrente a tutte le periferiche esterne.

Non si vuole fare una trattazione troppo dettagliata dell'architettura interna del microcontrollore in quanto già trattata dettagliatamente nella pagina relativa alla [Motion control](/project/motion-control) e si rimanda la visione a tale pagina.

I sensori esterni di cui è costituita la scheda sono i sensori infrarosso, e i sensori a ultrasuoni, questi andranno collegati alla scheda mediante i connettori visibili in figura sulla destra.