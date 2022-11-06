---
layout: page
title: Návod k IRdet
permalink: /cz/irdet-manual
lang: cz
hide: true
---

Modul IRdet slouží k připojení až 8 infračidel. Modul budí vysílací diody IR
čidel a kontroluje, jestli je čidlo zastíněno. Podle toho nastavuje
8 digitálních výstupů. Výstupy lze připojit například na vstupy modulu [MTB-UNI
v4](/cz/v4/uni). Modul není připojen na sběrnici MTBbus!

## Napájení, sběrnice

Modul je optimální napájet stabilizovaným napětím 12 V stejnosměrných. Modul
toleruje napájení 10–17 V stejnosměrných. Napájení se připojuje na svorky označené
"+12V" (kladný pól) a "GND" (záporný pól) na svorkovnicích. Svorkovnice
jsou na desce dvě. Je jedno, na kterou svorkovnici je napájení připojeno,
svorkovnice mají propojené vodiče pro snazší instalaci.

Modul *IRdet* obsahuje ochranu proti přepólování vstupního napětí (modul
nenaběhne). Modul neobsahuje ochranu proti přepětí!

## Infračidla

IRdet se používá pro detekci projetí vlaku bodem. Mezi pražce se umístí pár
*vysílací dioda – fototranzistor*. Vysílané světlo z diody se odrazí od
projíždějícího vozu, čímž je detekován průjezd.

Modul obsahuje 4 konektory, do každého lze zapojit pár čidel. Zapojení
doporučujeme realizovat podle obrázku níže.

<figure>
<img src="/assets/img/mtb4/irdet-example.svg" alt="Zapojení páru IR čidel" style="width: 100%; max-width: 500px" />
<figcaption>Zapojení páru IR čidel.</figcaption>
</figure>

Důrazně doporučujeme zkontrolovat, že všechny lokomotivy i vozy jsou správně
detekovány. Obzvláště u matných černých povrchů podvozků může být problém
vozidlo detekovat.

## Výstupy

Modul obsahuje binární výstup pro každé čidlo indikující obsazenost čidla.
Tento výstup je zapojený přes optický oddělovač v režimu *otevřený kolektor*
(aktivní = uzemněn).
