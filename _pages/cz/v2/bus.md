---
layout: page
title: Sběrnice MTBbus v2
permalink: /cz/v2/bus
lang: cz
hide: true
ref: bus
---

Komunikace mezi MTB moduly probíhá pomocí dvouvodičového rozhraní RS485.
V přenosu dat je použit devítibitový režim UART. Přenosová rychlost je 38.4 kBd
– 115 kBd, typický přenos jednoho příkazu a odpovědi mezi PC a modulem trvá cca
2 ms resp. 0.8 ms. Komunikace je založena na principu master-slave, tj. příkazy
vysílá výhradně MTB-USB modul jednotlivým modulům, které
zpětně odpoví. Každý modul má nastavenu unikátní adresu, pomocí které mu jsou
směrovány příkazy. Detailnější rozebírání komunikace již spadá mimo oblast
modelářství, znalost komunikace však není podmínkou ke stavbě a oživení modulů.

 * [Popis komunikace MTBbus v2.0](/assets/pdf/mtb-protok20.pdf)

---
**Pozor**: KMŽ Brno I momentálně (2020) využívá protokol v3.0, který na těchto
stránkách z licenčních důvodů nemůžeme uvést. v3.0 se od verze 2.0 zásadně
neliší: mění ID modulů, přidává víc rychlostí komunikace a přidává kontrolní
součty do odpovědí modulů.

---

## Nastavení adresy modulů MTBbus

Volba adresy u modulů MTB je řešena jednoduše zasunovacími propojkami. Výhodou
je snadnost nastavení, které je snadno "čitelné".

## Konfigurace funkce modulů MTBbus

Moduly mají možnost konfigurace (např. volba připojení různých typů vstupních
signálů), která je řešena programově. Po zapnutí řídící počítač zjistí, jaké
moduly jsou připojeny na sběrnici a každému nich pošle jeho konfigurační data.
Data jsou typicky uložena v PC a lze je proto při oživování a instalaci
jednoduše upravit. Výhodou řešení je odstranění různých procedur SW nastavování
modulů (jako u DCC) uložených do EEPROM.
