---
layout: page
title: MTB sběrnice
permalink: /bus
order: 30
lang: cz
ref: bus
---

Komunikace mezi MTB moduly probíhá pomocí dvouvodičového rozhraní RS485.
V přenosu dat je použit devítibitový režim UART podporovaný rozhraním procesoru
AT89C2051. Přenosová rychlost je 38.4 kBd – 115 kBd, typický přenos jednoho
příkazu a odpovědi mezi PC a modulem trvá cca 2ms resp. 0.8ms. Komunikace je
založena na principu master-slave, tj. příkazy vysílá výhradně počítač PC
(resp. MTB-USB modul) jednotlivým modulům, které zpětně odpoví. Každý modul má
nastavenu unikátní adresu, pomocí které mu jsou směrovány příkazy. Detailnější
rozebírání komunikace již spadá mimo oblast modelářství, znalost komunikace
však není podmínkou ke stavbě a oživení modulů.

 * [Popis komunikace MTBbus v2.0](/assets/pdf/mtb-protok20.pdf)

## Nastavení adresy modulů MTBbus

Volba adresy u modulů MTB je řešena jednoduše zasunovacími propojkami Výhodou
je snadnost nastavení, které je snadno "čitelné".

## Konfigurace funkce modulů MTBbus

Moduly mají možnost konfigurace (např. volba připojení různých typů vstupních
signálů), která je řešena programově. Po zapnutí řídící počítač zjistí, jaké
moduly jsou připojeny na sběrnici a každému nich pošle jeho konfigurační data.
Data jsou v PC uložena v textovém souboru a lze je proto při oživování
a instalaci jednoduše upravit. Více informací je uvedeno v popisu řídícího
programu PC.  Výhodou řešení je odstranění různých procedur SW nastavování
modulů (jako u DCC) uložených do EEPROM.
