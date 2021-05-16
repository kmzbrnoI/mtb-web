---
layout: page
title: Sběrnice MTBbus v4
permalink: /cz/v4/bus
lang: cz
order: 20
ref: bus
---

Komunikace mezi MTB moduly probíhá pomocí dvouvodičového rozhraní RS485.
V přenosu dat je použit devítibitový režim UART. Přenosová rychlost je 38.4 kBd
– 115 kBd. Komunikace je založena na principu master-slave, tj. příkazy
vysílá výhradně [MTB-USB deska](usb) jednotlivým modulům, které odpovídají.
Každý modul má nastavenu unikátní adresu, pomocí které mu jsou směrovány
příkazy. Detailnější rozebírání komunikace již spadá mimo oblast modelářství,
znalost komunikace však není podmínkou ke stavbě a oživení modulů.

 * [Popis komunikace MTBbus v4](https://github.com/kmzbrnoI/mtbbus-protocol)
   (anglicky)
 * [Seznam změn oproti verzi 2](https://github.com/kmzbrnoI/mtbbus-protocol/blob/master/changelog.md) (anglicky)

Sběrnice je navržena tak, aby v budoucnu umožňovala přidání dalších typů modulů.

## Nastavení adresy modulů MTB

Moduly MTB je možné adresovat buď zasouvacími propojkami, nebo z počítače.
Protokol umožňuje obě varianty, volba je na autorovi MTB modulu.

Např. modul [MTB-UNI v4](uni) používá pro volbu adresy zasouvací propojky.

## Konfigurace funkce modulů MTB

Moduly mají možnost konfigurace (např. volba připojení různých typů vstupních
signálů), která je řešena programově. Po zapnutí řídící počítač zjistí, jaké
moduly jsou připojeny na sběrnici a každému nich pošle jeho konfigurační data.
Data jsou typicky uložena v PC a lze je proto při oživování a instalaci
jednoduše upravit.
