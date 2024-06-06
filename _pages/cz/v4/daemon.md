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

## Konzolový konfigurátor MTB Daemona

Pro pokročilejší ovládání MTB Daemona, např. nastavení konfigurace MTB modulu,
je možné využít [konzolový skript `manage.py`](https://github.com/kmzbrnoI/mtb-daemon/blob/master/utils/manage.py).

Filosofie MTB Daemona je taková, že veškeré operace se provádějí skrze síťové
rozhraní. Zásahy do souboru `mtb-daemon.json` uživatelem by měly být minimální.

Skript je jednoduchá konzolová aplikace psaná v jazyce Python. Nezapomeňte si
tedy pro jeho běh nainstalovat Python.

<figure>
<img src="/assets/img/mtb4/manage-py-mtbusb.png" alt="Zjištění informací o MTB-USB skrze manage.py" style="width: 100%; max-width: 524px" />
<figcaption>Příklad: zjištění informací o MTB-USB skrze `manage.py`.</figcaption>
</figure>

Více informací o použití `manage.py` lze vyčíst buď po spuštění
`manage.py --help` nebo přímo ze [zdrojového
kódu](https://github.com/kmzbrnoI/mtb-daemon/blob/master/utils/manage.py).

## Okénkový konfigurátor MTB Daemona

Okénkový konfigurátor MTB Daemona je v přípravě ve spolupráci s kolegou Michalem
Petrilakem.
