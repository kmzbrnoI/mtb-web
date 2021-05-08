---
layout: page
title: MTB-USB v4
permalink: /v4/usb
order: 21
lang: cz
ref: usb
---

MTB-USB poskytuje rozhraní mezi sběrnici [MTBbus](bus) a počítačem (USB). Řeší
časově kritické operace sběrnice a umožňuje SW v počítači povelovat MTB moduly.

<figure>
<img src="/assets/img/mtb4/usb-all.jpg" alt="Modul MTB-USB" style="max-width: 500px">
<figcaption>MTB-USB v4</figcaption>
</figure>

<figure>
<img src="/assets/img/mtb4/usb-inside.jpg" alt="Modul MTB-USB" style="max-width: 500px">
<figcaption>DPS MTB-USB v4</figcaption>
</figure>

MTB-USB obsahuje galvanické oddělení počítačové a sběrnicové části. Počítačová
část je napájena přímo z USB, sběrnicová část je napájena buď ze stejného rozvodu
jako MTB moduly nebo galvanicky odděleným měničem z počítačové části (variantní
osazení součástek). Srdcem desky je procesor *STM32F103* v počítačové části,
který je programován v jazyce C.

Veškerá výrobní data k modulu jsou k dispozici ve zdrojových formátech.

 * [Schéma zapojení modulu a výkres desky plošných spojů](https://github.com/kmzbrnoI/mtb-usb-4-pcb)
 * [Firmware](https://github.com/kmzbrnoI/mtb-usb-4-fw)
