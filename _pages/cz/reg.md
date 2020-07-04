---
layout: page
title: Modul MTB-REG
permalink: /cz/reg
order: 53
lang: cz
ref: reg
---

Modul regulátoru jízdy (občas nazývaný také stacionární dekodér) je koncipován
jako 8-kanálový PWM regulátor s oboupolaritním výstupem (společná kolejnice
s 0V potenciálem). Modul umožňuje řídit analogové lokomotivy. Díky stále
většímu zastoupení digitálního řízení kolejiště je tento modul v roce 2020
spíše historickou ukázkou, než modulem reálně používaným v kolejištích. V roce
2020 v KMŽ Brno I žádný takový modul není nasazen.

Základní deska obsahuje CPU pro příjem příkazů a generování řídícího signálu
a připojovací konektory. Do zásuvných konektorů jsou vkládány 4 výkonové moduly,
z nichž každý obsahuje výkonové polovodiče pro spínání trakce pro dva kanály.
Výkonové moduly mají galvanicky oddělené trakční napájení od komunikace MTBbus
a vestavěnou detekci přetížení. Při přetížení se rozsvítí LED, CPU sníží napětí
na výstupu a zahlásí chybu prostřednictvím sběrnice MTBbus do centrálního PC.

Při poškození výkonových modulů lze snadno provést výměnu náhradou za jiný.

 * [Detailní popis modulu MTB-REG v2.1](/assets/pdf/mtb-reg21.pdf)
 * [Schéma modulu MTB-REG v2.1](TODO)
 * Firmware TODO

<figure>
<img src="/assets/img/mtbreg21pwr.jpg" alt="Modul MTB-REG v2.1" style="max-width: 300px" />
<figcaption>Modul MTB-REG v2.1</figcaption>
</figure>
