---
layout: page
title: Základní informace
permalink: /cz/index
lang: cz
ref: index
---

MTB je systém pro řízení příslušenství modelového kolejiště. Jeho cílem je
zpracovat velké množství vstupů v kolejišti (např. detekci obsazení ) a umožnit
nastavit velké množství výstupů v kolejišti (např. výhybky). Systém je typicky
řízený z počítače, ve kterém běží SW zabezpečující provoz.

Systém MTB se skládá z:

 * [vstupně/výstupních modulů](/cz/modules),
 * [MTB-USB desky](/cz/usb) pro připojení systému k počítači,
 * [počítačových knihoven](/cz/lib) pro přístup k sběrnici,

![Obrázek topologie sběrnice]()

MTB moduly komunikují po sběrnici [MTBbus](/cz/bus).

Moduly jsou zabudovány přímo v kolejišti, co nejblíže umístění ovládaných
prvků a snímaných signálů. Kabeláž ke každému modulu se skládá ze dvou
vodičů RS485 a napájení 12 V (s případným doplněním -12 V napětí pro trakční
regulátory). Díky zjednodušení propojení na pouhé 4 (5) vodičů je snadné
zabudovat MTBbus komponenty do rozkládacího příp. modulového kolejiště, přičemž
vlastní propojení se zajistí pomocí 4(5)-pólových konektorů.

Kolejiště s počítačem propojuje USB kabel. Při pohledu na jednoduchost rozvodů
je ihned vidět první přednost digitální komunikace v porovnání s dřívějšími
svazky vodičů.

Autorem systému MTB je Víťa Báňa (KŽM Praha 3), systém byl dále rozšířen Petrem
Trávníkem (KMŽ Brno I). Tento web přebírá informace z původního webu
`http://www.volny.cz/mtbbus/mtb/mtb-hw2.htm` Víti Báni, který nyní již není
dostupný. Tento web představuje systém MTB ve verzi, v~jaké je v~současnosti
nasazen v~KMŽ Brno I.

Cílem tohoto webu je systém MTB představit.

## Základní vlastnosti

 * Sběrnice umožňuje snímání digitálních i analogových vstupů v kolejišti.
 * Sběrnice umožňuje řízení digitálních výstupů a S-COM návěstidel.
 * Typický modul má 16 digitálních vstupů a 16 digitálních výstupů.
 * Až 256 modulů.
 * Sběrnice RS485.
