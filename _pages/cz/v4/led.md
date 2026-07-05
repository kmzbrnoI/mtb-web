---
layout: page
title: Modul MTB-LED
permalink: /cz/v4/led
lang: cz
order: 27
ref: led
---

Modul MTB-LED umožňuje připojení 32 LED. Předpokládané využití je ovládání
stacionárního osvětlení – pouliční osvětlení, osvětlení domů, budov atd.

<figure>
<img src="/assets/img/mtb4/uni-v40-screw-all.jpg" alt="Modul MTB-LED" style="width: 100%; max-width: 500px" />
<figcaption>Modul MTB-LED</figcaption>
</figure>

## Vlastnosti

 * 32 samostatně řízených výstupů.
 * Proudový zdroj 20 mA.
 * V konfiguraci modulu je u každého výstupu možné samostatně nastavit PWM
   připojení proudového zdroje v rozsahu 1–255.
 * K výstupům se připojuje záporný pól LED, kladný pól je společný pro všechny LED (okruhy).
 * Možnost připojit více LED v jednom okruhu v sérii (typicky až 5 žlutých LED v okruhu).
 * LED nepotřebují žádné další externí součástky – rezistory apod., do modulu se připojují přímo LED.
 * Napájení: 7–17 V DC.
 * Softwarová adresa na MTBbus.
 * Náklady na výrobu: ~?00 Kč.
 * Typická prodejní cena sestaveného a otestovaného kusu: ??? Kč.

Srdcem modulu je procesor ATmega328p, který obsahuje všechny potřebné funkce
pro řízení a komunikaci. Připojení LED, MTBbus a napájení je realizováno pomocí zásuvných
šroubových svorkovnic. Napájení a MTBbus lze připojit na libovolný z konektorů
J2 a J4. K ovládání LED výstupů jsou využity obvody TLC5940.

Veškerá výrobní data modulu jsou k dispozici pod otevřenou licencí.

 * [Schéma a deska plošných spojů](https://github.com/kmzbrnoI/mtb-led-hw)
 * [Firmware](https://github.com/kmzbrnoI/mtb-led-fw)

<div style="text-align:center;">
<a class="btn" style="width:200px; margin: 10px;" href="/cz/poridit">Chci si pořídit MTB-LED</a>
</div>
