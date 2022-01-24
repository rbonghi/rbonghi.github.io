---
title: "Enigma"
excerpt: "(:it: in Italian) Enigma was my first minisumo project for didactics. The core of this robot was two different controller. The first one with BEAM technology (only two transistor control the robot movement inside the ring and find the enemy. The last one with an little micro 16F628A for expriment in Basic and C."
permalink: /robot/enigma
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  teaser: /assets/robot/enigma/Enigma2.jpg
  overlay_image: /assets/robot/enigma/enigma-robofesta2.jpg
  actions:
    - label: "🌐 minisumo.net"
      url: "https://minisumo.net/"
premi:
  - url: /assets/robot/enigma/premi/2006Neumann2.jpg
    image_path: /assets/robot/enigma/premi/2006Neumann2.jpg
    alt: "2006 Von Neumann - 2 posto"
    title: "2006 Von Neumann - 2 posto"
  - url: /assets/robot/enigma/premi/2006Pisa2.jpg
    image_path: /assets/robot/enigma/premi/2006Pisa2.jpg
    alt: "2006 Pisa - 2 posto"
    title: "2006 Pisa - 2 posto"
  - url: /assets/robot/enigma/premi/2008Neumann3.jpg
    image_path: /assets/robot/enigma/premi/2008Neumann3.jpg
    alt: "2008 Von Neumann - 3 posto"
    title: "2008 Von Neumann - 3 posto"
---

E' il robot più piccolo della famiglia, ma uno di quelli più agguerriti. Nasce nel dicembre del 2003 con l'idea di fare un robot del tipo BEAM (senza microcontrollore) e per imparare le prime nozioni di elettronica, partendo dai condensatori fino ad arrivare al transistor. Ero uno studente del liceo classico e tutto ciò era difficile da apprendere.

{% include figure image_path="/assets/robot/enigma/primaversione.jpg" alt="Enigma telaio" caption="Enigma telaio" %}

Il telaio partiva da una versione commerciale di [robot-italy](http://www.robot-italy.com/), questa era costituita da vari pezzi in plexy tagliati a laser (nella figura precedente) ed era azionato da due servocomandi modificati (senza l'elettronica). L'elettronica, era il primo vero esercizio di saldatura su millefori e come tale le saldature e la disposizioni dei componenti lasciavano a desiderare.

{% include figure image_path="/assets/robot/enigma/enigma-millefori.jpg" alt="Enigma millefori" caption="Enigma millefori" %}

Nel corso dei vari test e di più e più schede saldate si iniziò a veder funzionare il robot, ma non ottenne mai i successi sperati, molto spesso veniva battuto da robot di altri concorrenti o da [NX-01](/robot/NX-01). Nel 2006 si iniziò a riprogettare il robot cercando di essere più competitivo rispetto alla precedente versione, l'idea era quella di poter realizzare una guida didattica sulla costruzione di questo robot, il progetto quindi si divise in varie fasi, da una riprogettazione meccanica, e di una elettronica BEAM ed una seconda digitale con un microcontrollore.

La guida venne divisa in più parti, dalla progettazione del telaio venne realizzata la guida per farsi la scheda BEAM di controllo del robot (questa volta senza usare millefori) ed infine  la scheda di controllo con il 16F84A. Il robot era dotato di due sensori di linea QRB1134 e due sensori per riconoscere l'avversario dati dai GP2D15.

{% include figure image_path="/assets/robot/enigma/Enigma2.jpg" alt="Enigma prima versione" caption="Enigma prima versione" %}

Ma durante le gare, e per carenza di sensori riutilizzati per progetti successivi ([Slider](/robot/slider)) i sensori per riconoscere l'avversario vennero rimossi, ed incredibilmente pur navigando cieco all'interno del campo rimaneva sufficientemente forte da spingere gli avversari al di fuori del ring. Durante l'eurobot 2006 di Catania organizzato da Minisumo.net il robot Enigma sponsorizzato per l'evento.

{% include figure image_path="/assets/robot/enigma/enigma-robofesta2.jpg" alt="Enigma Catania" caption="Enigma Catania" %}

Non tutti i robot però riusciva il robot a battere, infatti [Dark Blade](/robot/dark-blade) rimaneva uno dei peggiori robot da poter sconfiggere.

Enigma è comunque riuscito a vincere vari premi nel corso della sua carriera, qui una breve lista delle sue vittorie.

{% include figure image_path="/assets/robot/enigma/enigma-Robofesta.jpg" alt="Enigma vs Dark Blade" caption="Enigma vs Dark Blade" %}

# Premi

{% include gallery id="premi" caption="Enigma premi" %}