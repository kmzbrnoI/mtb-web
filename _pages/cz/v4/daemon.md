---
layout: page
title: MTB Daemon
permalink: /cz/v4/daemon
order: 51
lang: cz
ref: daemon
---

*MTB Daemon* je počítačová konzolová aplikace, která umožňuje propojení
[MTB-USB](usb) s řídicími softwary kolejiště, např. hJOP. MTB Daemon uchovává
konfiguraci MTB modulů. K aplikaci se může připojit více programů řídících MTB
moduly, například software zabezpečující řízení železniční dopravy (např.
hJOP), software řídící osvětlení, software řídící tramvajovou dopravu apod.
Jediná sběrnice MTBbus může tedy být sdílena pro více ovládaných systémů
s oddělenými řídicími softwary, což umožňuje ekonomičtější a jednodušší instalaci.

<a class="btn" href="https://github.com/kmzbrnoI/mtb-daemon/releases">Stáhnout</a>

<blockquote>
PC aplikace se obecně může připojit k MTB-USB i přímo, bez využití MTB Daemona, ale
doporučené řešení je využít MTB Daemona. Např. hJOP umožňuje pouze připojení
pomocí MTB Daemona, přímé připojení k MTB-USB neumožňuje.
</blockquote>

Řídicí programy se připojují k MTB Daemonu přes trvale otevřené TCP spojení,
lze je tedy umístit i na jiný počítač.

 * [Specifikace protokolu pro připojení klientů](https://github.com/kmzbrnoI/mtb-daemon/tree/master/tcp-protocol)
 * [Zdrojové kódy MTB Daemon](https://github.com/kmzbrnoI/mtb-daemon)

Celková architektura použití systému MTB s aplikací MTB Dameon vypadá takto:

<figure>
<img src="/assets/img/mtbv4-topology.svg" alt="Celková architektura MTB" style="width: 100%; max-width: 600px" />
<figcaption>Celková architektura MTB.</figcaption>
</figure>

*hJOP* je software řídící provoz kolejiště. *MTB Net Lib* je knihovna propojující
*hJOP* a *MTB Daemon*, ke stažení [zde](https://github.com/kmzbrnoI/mtb-net-lib).

## Spuštění MTB Daemona

MTB Daemon je konzolová aplikace. Na Windows je doporučeno její spuštění po
zapnutí PC na pozadí. K tomuto můžete využít např. Win+R a dále `shell:startup`.

<figure>
<img src="/assets/img/mtb4/mtb-daemon-default.png" alt="mtb-daemon.exe po spuštění" style="width: 100%; max-width: 800px" />
<figcaption>mtb-daemon.exe po spuštění.</figcaption>
</figure>

`mtb-daemon.exe` přebírá jediný nepovinný argument – cestu k hlavnímu
konfiguračnímu souboru. Výchozí hodnota je `mtb-daemon.json`. Specifikace formátu
souboru je [zde](https://github.com/kmzbrnoI/mtb-daemon/blob/master/doc.mtb-daemon.json.md).

Po zapnutí MTB Daemona je možné se k daemonu připojit, např. ze SW hJOP pomocí
mtb-net-lib.

## Konfigurace MTB Daemona

Konfigurace MTBbus a MTB modulů doporučujeme provádět pomocí jedné z konfiguračních
aplikací:

* [Okénková aplikace MTB Config Tool](/cz/v4/config-tool)
* [Konzolová aplikace manage.py](/cz/v4/manage-py)

MTB Daemon si veškerou konfiguraci ukládá do textového souboru `mtb-daemon.json`.
Tento soubor obecně nedoporučujeme upravovat ručně, za pozornost k ruční úpravě
však stojí sekce mimo sekci `modules`. Např. v `server/allowedClients` lze vyjmenovat
IP adresy klientů, kteří mají mít přístup ke sběrnici pro zápis.
