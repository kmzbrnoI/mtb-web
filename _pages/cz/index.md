---
layout: page
title: Systém MTB
permalink: /index
lang: cz
ref: index
---

MTB je systém pro řízení příslušenství modelového kolejiště. Jeho cílem je
zpracovat velké množství vstupů v kolejišti (např. detekce obsazení,
signalizace polohy přestavníků, ...) a umožnit nastavit velké množství výstupů
v kolejišti (např. výhybky, návěstidla, ...). Systém je typicky řízený z počítače, ve kterém
běží SW zabezpečující provoz.

Systém MTB se skládá z:
 * [vstupně/výstupních modulů](/modules),
 * [MTB-USB desky](/usb) pro připojení systému k počítači,
 * [počítačových knihoven](/lib) pro přístup k sběrnici,

<figure>
<img src="/assets/img/topology.svg" alt="Topologie sběrnice MTBbus" style="max-width: 600px" />
<figcaption>Topologie sběrnice MTBbus.</figcaption>
</figure>

MTB moduly komunikují po sběrnici [MTBbus](/bus).

Moduly jsou zabudovány přímo v kolejišti, co nejblíže umístění ovládaných
prvků a snímaných signálů. Kabeláž ke každému modulu se skládá ze dvou
vodičů RS485 a napájení 12 V (s případným doplněním -12 V napětí pro trakční
regulátory). Díky zjednodušení propojení na pouhé 4 (5) vodičů je snadné
zabudovat MTBbus komponenty do rozkládacího příp. modulového kolejiště, přičemž
vlastní propojení se zajistí pomocí 4(5)-pólových konektorů.

Kolejiště s počítačem propojuje USB kabel. Při pohledu na jednoduchost rozvodů
je ihned vidět první přednost digitální komunikace v porovnání s dřívějšími
svazky vodičů.

Autorem systému MTB je Víťa Báňa (KŽM Praha 3), systém byl dále rozšířen Petrem
Trávníkem (KMŽ Brno I). Tento web přebírá informace z původního webu
`http://www.volny.cz/mtbbus/mtb/mtb-hw2.htm` Víti Báni, který nyní již není
dostupný. Tento web představuje systém MTB ve verzi, v jaké je v současnosti
nasazen v KMŽ Brno I.

## Základní vlastnosti systému MTB

 * Snímání digitálních i analogových vstupů z kolejiště.
 * Řízení digitálních výstupů a S-COM návěstidel.
 * Typicky 16 digitálních vstupů a 16 digitálních výstupů na modul.
 * Až 256 modulů.
 * Sběrnice RS485.
