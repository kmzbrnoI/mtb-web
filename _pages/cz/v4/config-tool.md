---
layout: page
title: MTB Config Tool
permalink: /cz/v4/config-tool
order: 52
lang: cz
ref: daemon
---

Novinka 2024.

*MTB Config Tool* neboli *MTB Konfigurační Nástroj* je grafická aplikace umožňující
konfigurovat MTB-USB a MTB moduly. Připojuje se k MTB Daemonu standardním síťovým
připojením.

<a class="btn" href="https://github.com/kmzbrnoI/mtb-config-tool/releases">Stáhnout</a>
<a class="btn" href="https://github.com/kmzbrnoI/mtb-config-tool">Repozitář se zdrojovými kódy</a>

<figure>
<img src="/assets/img/mtb4/mtb-config-tool/main-window-cz.png" alt="Hlavní okno MTB Config Tool v češtině" style="width: 100%;" />
<figcaption>Hlavní okno MTB Config Tool v češtině na OS Windows.</figcaption>
</figure>

## Základní funkce

* Zobrazení aktuálního stavu MTB Daemona.
  - Připojení k MTB-USB, verze FW MTB-USB, verze MTBbus protokolu.
* Konfigurace MTB-USB: vyčtení rychlosti MTB-USB, změna rychlosti.
* Zobrazení aktuálního stavu všech MTBbus modulů.
  - Název modulu, adresa, verze FW, verze bootloaderu, aktivní porucha, varování,
    maják.
* De/aktivace majáku modulu.
* Konfigurace modulu.
  - Podporované moduly: MTB-UNI, MTB-UNIS.
* Restart modulu.
* Čtení diagnostiky modulu.
* Změna adresy modulu.
* Aktualizace FW modulu.
* Přidání nového modulu, odstranění modulu.
* Český a anglický jazyk.

## Ukázka aplikace

<figure>
<img src="/assets/img/mtb4/mtb-config-tool/main-window-linux.png" alt="Hlavní okno MTB Config Tool" style="width: 100%;" />
<figcaption>Hlavní okno MTB Config Tool v angličtině na OS Linux.</figcaption>
</figure>

<figure>
<img src="/assets/img/mtb4/mtb-config-tool/mtb-uni-v2-config.png" alt="Konfigurace modulu typu MTB-UNI v2" style="height: 650px;" />
<figcaption>Konfigurace modulu typu MTB-UNI v2.</figcaption>
</figure>

<figure>
<img src="/assets/img/mtb4/mtb-config-tool/mtb-uni-v2-diag.png" alt="Diagnostika modulu typu MTB-UNI v2" style="width: 100%;" />
<figcaption>Diagnostika modulu typu MTB-UNI v2.</figcaption>
</figure>
