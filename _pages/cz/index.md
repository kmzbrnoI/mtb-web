---
layout: page
title: Systém MTB
permalink: /index
lang: cz
ref: index
---

MTB je systém pro řízení příslušenství modelového kolejiště. MTB zpracovává
vstupy z kolejiště (např. detekce obsazení kolejových obvodů, signalizace
polohy přestavníků, ...) a nastavuje výstupy v kolejišti (např. výhybky,
návěstidla, ...). Systém je typicky řízený z počítače, ve kterém běží SW
zabezpečující provoz. MTB neřídí jízdu vlaku, řídí pouze příslušenství
v kolejišti.

**Systém MTB v roce 2021 zaznamenal výraznou aktualizaci. Vzniklo *MTB v4*.
Tento web popisuje novou verzi 4, dokumentace starší verze 2 je dostupná
[zde](v2).**

Systém MTB se skládá z:
 * [vstupně/výstupních modulů](/v4/modules),
 * [MTB-USB desky](/v4/usb) pro připojení systému k počítači,
 * [počítačových aplikací a knihoven](/v4/daemon) pro přístup ke sběrnici.

<figure>
<img src="/assets/img/mtbv4-topology.svg" alt="Topologie sběrnice MTBbus" />
<figcaption>Topologie sběrnice MTBbus.</figcaption>
</figure>

MTB moduly komunikují po sběrnici [MTBbus](/v4/bus).

Moduly jsou zabudovány přímo v kolejišti, co nejblíže ovládaných
prvků a snímaných signálů. Kabeláž ke každému modulu se skládá ze dvou
vodičů RS485 a napájení 12 V. Díky zjednodušení propojení na pouhé 4 vodiče
je snadné zabudovat MTBbus komponenty do rozkládacího příp. modulového
kolejiště, přičemž vlastní propojení se zajistí pomocí 4pólových konektorů.

Sběrnice MTBbus je řízená *master* deskou [MTB-USB](v4/usb). Zatím existují tyto
moduly:

 * [MTB-UNI](v4/uni)
 * [Rozšíření deskek MTB-UNI, MTB-UNIm a MTB-TTL v2 pro použití s MTB v4](v4/mtb-2-avr)

## Základní vlastnosti systému MTB

 * Snímání digitálních vstupů z kolejiště.
 * Řízení digitálních výstupů a [S-COM](https://www.mtb-model.com/elektro/s-com.htm) návěstidel.
 * Až 255 modulů, celkem až 4080 vstupů a 4080 výstupů.
 * Sběrnice RS485.
 * Detekce funkčnosti modulů.
 * Aktualizace firmware modulů přímo přes [MTBbus](v4/bus).
 * Výměna modulů možná za chodu sběrnice.
 * Otevřené řešení, všechna výrobní data pro všechny komponenty k dispozici.
