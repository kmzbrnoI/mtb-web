---
layout: page
title: Systém MTB
permalink: /index
lang: cz
ref: index
---

MTB je systém pro řízení příslušenství modelového kolejiště. Jeho cílem je
zpracovat velké množství vstupů v kolejišti (např. detekce obsazení kolejových
obvodů, signalizace polohy přestavníků, ...) a umožnit nastavit velké množství
výstupů v kolejišti (např. výhybky, návěstidla, ...). Systém je typicky řízený
z počítače, ve kterém běží SW zabezpečující provoz. MTB neřídí jízdu vlaku, řídí
pouze příslušenství v kolejišti.

**Systém MTB v roce 2021 zaznamenal výraznou aktualizaci. Vzniklo *MTB v4*.
Tento web popisuje novou verzi 4, dokumentace starší verze 2 je dostupná
[zde](v2).**

Systém MTB se skládá z:
 * [vstupně/výstupních modulů](/v4/modules),
 * [MTB-USB desky](/v4/usb) pro připojení systému k počítači,
 * [počítačových aplikací a knihoven](/v4/pc) pro přístup k sběrnici,

<figure>
<img src="/assets/img/topology.svg" alt="Topologie sběrnice MTBbus" style="max-width: 600px" />
<figcaption>Topologie sběrnice MTBbus.</figcaption>
</figure>

MTB moduly komunikují po sběrnici [MTBbus](/v4/bus).

Moduly jsou zabudovány přímo v kolejišti, co nejblíže umístění ovládaných
prvků a snímaných signálů. Kabeláž ke každému modulu se skládá ze dvou
vodičů RS485 a napájení 12 V. Díky zjednodušení propojení na pouhé 4 vodiče
je snadné zabudovat MTBbus komponenty do rozkládacího příp. modulového
kolejiště, přičemž vlastní propojení se zajistí pomocí 4pólových konektorů.

Autorem systému MTB je Víťa Báňa (KŽM Praha 3), systém byl dále rozšířen Petrem
Trávníkem (KMŽ Brno I). Tento web přebírá informace z původního webu
`http://www.volny.cz/mtbbus/mtb/mtb-hw2.htm` Víti Báni, který nyní již není
dostupný. Tento web představuje systém MTB ve verzi, v jaké je v současnosti
nasazen v KMŽ Brno I.

## Základní vlastnosti systému MTB

 * Snímání digitálních i analogových vstupů z kolejiště.
 * Řízení digitálních výstupů a S-COM návěstidel.
 * Typicky 16 digitálních vstupů a 16 digitálních výstupů na modul.
 * Až 255 modulů.
 * Sběrnice RS485.
