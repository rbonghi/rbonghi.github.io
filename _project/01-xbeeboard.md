---
title: "Xbee Board"
excerpt: "(:it: in Italian) Its an expansion shield for Xbee module. This board have inside a power regulator from 5V to 3.3V and three different leds to recognize the status of the radio module."
permalink: /project/xbeeboard/
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2006
header:
  teaser: /assets/project/xbeeboard/XBee.jpg
---

Questa scheda adatta la piedinatura del modulo radio prodotto dalla Digi® al Bus di comunicazione presente sul modulo della Motion Control.

{% include figure image_path="/assets/project/xbeeboard/ModuloXbee-rendering.png" alt="Rendering Xbee board" caption="Rendering Xbee board" %}

Il modulo XBee è una soluzione compatibile con lo standard ZigBee/IEEE 802.15.4 ed opera nella banda ISM alla frequenza di 2.4GHz. Il modulo è semplice da utilizzare, richiede pochissima energia e costituisce una soluzione efficace ed affidabile per la trasmissione dei dati. La configurazione di base supporta una vasta gamma di applicazioni di trasmissione dati. Utilizzando i comandi AT, è possibile riconfigurare il modulo ed accedere a funzioni avanzate.

{% include figure image_path="/assets/project/xbeeboard/strutturaxbee.jpg" alt="Architettura xbee" caption="Archiettura xbee" %}

Il primo vantaggio consiste nel fatto che i moduli XBee sono bidirezionali (come è visibile nell'immagine seguente). Parecchi sistemi economici a 433MHz sono unidirezionali, ed in questo caso con questo sistema il trasmettitore non ha idea se il ricevitore stia ricevendo i dati o meno.

Ogni XBee ha un numero seriale univoco. Questo significa che 2 o più unita possono essere settate per parlare esclusivamente tra loro, ignorando tutti i segnali di altri moduli. Infine questi moduli possiedono una logica precostruita all'interno, dove sono già implementati tutti i necessari controlli tipici di una trasmissione wireless, quali ad esempio l'error checking.

Caratteristiche Tecniche complessive:
* Frequenza operativa 2.4 GHz;
* Potenza RF 1 mW (0 dBm) (fino a 100m di portata);
* Range di temperatura industriale (-40 deg, 85 deg);
* Supportate modalità di rete avanzate e basso consumo;
* Connessione Seriale, Controllo Sleep, CTS, RTS;
* Led RSSI, ON/SLEEP e Associate;