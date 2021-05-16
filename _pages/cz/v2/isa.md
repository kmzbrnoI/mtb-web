---
layout: page
title: Zásuvná karta RS485 do sběrnice ISA
permalink: /cz/v2/isa
lang: cz
hide: true
ref: isa
---

Zásuvná karta do ISA sběrnice tvořila prapůvodní propojovací rozhraní mezi
počítačem a sběrnicí MTBbus. Karta obsahuje mikrokontrolér se sériovým
rozhraním RS485, pomocí které se realizuje protokol MTBbus a současně zajišťuje
pomocné činnosti, které odlehčí funkce výkonnému programu v PC. Volba karty do
ISA slotu jako komunikačního rozhraní pro MTBbus vznikla z dříve realizovaného
projektu, což zjednodušilo a zrychlilo návrh prototypu. ISA sběrnice je však
dnes nedostupná, takže náhradou je [MTB-USB](usb) modul.

<figure>
<img src="/assets/img/mtbisa_foto.jpg" alt="Karta do sběrnice PC-ISA s komunikací RS485" style="max-width: 300px" />
<figcaption>Karta do sběrnice PC-ISA s komunikací RS485</figcaption>
</figure>
