---
title: "RegBoard"
excerpt: "(:it: in Italian) The regulation board is used to convert the tension from lithium batteries for all high level electronics boards. This board use a LM2576 produced from TI was used for Ottobot and Explorer robots."
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2006
header:
  teaser: /assets/project/regboard/regboard2_0.jpg
---

Il sistema di alimentazione costituito da un sistema di batterie al litio che erogano una tensione continua nominale di 14.8 volt e da un regolatore switching montato sulla scheda "Reg Board", della categoria dei convertitori DC/DC, (in figura) assicura la corretta erogazione di energia per tutte le varie componentistiche elettroniche, ad eccezione dei motori che sono alimentati dal "H-Bridge". Questa scelta risulta migliore in confronto all'impiego di un regolatore lineare, che dissiperebbe una potenza maggiore rispetto a quella richiesta dalla piattaforma.

{% include figure image_path="/assets/project/regboard/regboard2_0.jpg" alt="Regulation board" caption="Regulation board" %}

Il vantaggio di questa tecnica è di ridurre drasticamente la potenza dissipata dal circuito limitatore, rispetto all'impiego di transistor controllati analogicamente. In un circuito PWM (Pulse With Modulation), il transistor in un istante conduce completamente, riducendo al minimo la caduta ai suoi capi, oppure non conduce, annullando la corrente, ed in entrambi i casi la potenza dissipata è minima. In uscita tale regolatore, come verrà spiegato in Convertitori DC/DC necessita di un filtro passivo di tipo LC (tale filtro è in realtà LRC con la resistenza costituita dal conduttore dell'induttanza di pochi ohm) per poter ottenere un segnale il più possibile lineare ai capi degli altri dispositivi presenti sulla piattaforma mobile. Riferimenti in letteratura sulla progettazione di alimentatori in fondo alla pagina. Si è utilizzato il regolatore switching integrato prodotto dalla National il LM2576, che dispone delle ridotte dimensioni e delle caratteristiche necessarie per soddisfare le specifiche del progetto. Il filtro passa basso è stato realizzato con un'induttanza di $L =20 \mu H$ e un condensatore $C = 100\mu F$ visibili in figura.

# Test di valutazione

La "Reg Board" è alimentata a monte da un alimentatore lineare da 15 volt di uscita. In uscita la tensione è impostata a 5.000 volt, su un carico resistivo da 3.3 Ohm e poi da 1.65 Ohm (resistori corazzati da 50 W). Il ripple è misurato ai capi del carico, accoppiamento AC (nell’immagine seguente sono presenti la scheda ed i resistori)

{% include figure image_path="/assets/project/regboard/bancoregboard.jpg" alt="Banco di prova" caption="Banco di prova" %}

Vengono effettuate due misurazioni:

## Ripple misurato ai capi del carico - 1.5A

L’ampiezza picco-picco è di 40mV, alla frequenza circa 50 kHz. Con una tensione in uscita continua di Vout=5V, ed una corrente assorbita 1.5A. Questo porta a soddisfare pienamente le caratteristiche richieste in fase di sviluppo della scheda, come è possibile vedere nella immagine.

{% include figure image_path="/assets/project/regboard/Regboard-lisa0008.jpg" alt="Carico 1.5A" caption="Carico 1.5A" %}

## Ripple misurato ai capi del carico - 3.0A

L'ampiezza picco picco è di 40mV, frequenza circa 50 kHz. Con una tensione in uscita continua di Vout=5V, ed una corrente assorbita 3.0A. Nonostante la corrente limite, non ci sono variazioni significative sull'ampiezza del ripple d'uscita (circa 45-50mV), nella immagine.

{% include figure image_path="/assets/project/regboard/Regboardlisa0010.jpg" alt="Carico 3A" caption="Carico 3A" %}

# Rendimento

Con una corrente richiesta di circa I approx 1.3 A

$P_{in} = 0.676A \cdot 14.45V \approx 9.76 W$

$P_{out} = 1.355A \cdot 4.94V \approx 6.7 W$

$\eta = 69%$

Con correnti maggiori la scheda risulta avere una efficienza migliore:

$P_{in} = 1.36A \cdot 14.48V \approx 23.1 W$

$P_{out} = 2.54A \cdot 4.91V \approx 19.7 W$

$\eta = 85%$

# Analisi comportamento termico

Nell'ultima figura è possibile vedere, grazie alla termografia, le sollecitazioni termiche cui sono sottoposti i vari componenti elettronici durante un assorbimento di $I \approx 2.5A$.

{% include figure image_path="/assets/project/regboard/regboard3.jpg" alt="Regulation board temperatura" caption="Regulation board temperatura" %}
