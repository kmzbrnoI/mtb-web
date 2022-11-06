---
layout: page
title: MTB-USB v4
permalink: /cz/v4/usb
order: 21
lang: cz
ref: usb
---

MTB-USB poskytuje rozhraní mezi sběrnici [MTBbus](bus) a počítačem (USB). Řeší
časově kritické operace sběrnice a umožňuje SW v počítači povelovat MTB moduly.

<figure>
<img src="/assets/img/mtb4/usb-all.jpg" alt="Modul MTB-USB" style="width: 100%; max-width: 500px">
<figcaption>MTB-USB v4</figcaption>
</figure>

<figure>
<img src="/assets/img/mtb4/usb-inside.jpg" alt="Modul MTB-USB" style="width: 100%; max-width: 500px">
<figcaption>DPS MTB-USB v4</figcaption>
</figure>

MTB-USB obsahuje galvanické oddělení počítačové a sběrnicové části. Počítačová
část je napájena přímo z USB, sběrnicová část je napájena buď ze stejného rozvodu
jako MTB moduly nebo galvanicky odděleným měničem z počítačové části (variantní
osazení součástek). Srdcem desky je procesor *STM32F103* v počítačové části,
který je programován v jazyce C.

 * Napájení: 7–17 V DC.
 * Náklady na výrobu: ~1000 Kč.
 * Prodejní cena sestaveného a otestovaného kusu: 2000 Kč.

V počítači se MTB-USB tváří jaké sériový port, lze se k němu tedy připojit
z běžných operačních systémů (např. Windows a Linux) bez použití speciálních
ovladačů. Specifikace protokolu mezi MTB-USB a počítačem je k dispozici
[zde](https://github.com/kmzbrnoI/mtbbus-protocol/tree/master/pc).

Veškerá výrobní data k modulu jsou k dispozici ve zdrojových formátech.

 * [Schéma zapojení modulu a výkres desky plošných spojů](https://github.com/kmzbrnoI/mtb-usb-4-pcb)
 * [Schéma ve formátu PDF](https://github.com/kmzbrnoI/mtb-usb-4-pcb/releases/latest/download/mtb-usb-4-ele.pdf)
 * [Firmware](https://github.com/kmzbrnoI/mtb-usb-4-fw)

<div style="text-align:center;">
<a class="btn" style="width:300px; margin: 10px;" href="/cz/poridit">Chci si pořídit MTB-USB v4</a>
</div>
