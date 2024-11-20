---
layout: page
title: manage.py
permalink: /cz/v4/manage-py
order: 53
lang: cz
ref: daemon
---

Pro ovládání MTB Daemona, např. nastavení konfigurace MTB modulu, zapnutí majáku
nebo aktualizaci FW modulu je možné využít
[konzolovou aplikaci `manage.py`](https://github.com/kmzbrnoI/mtb-daemon/blob/master/utils/manage.py).

Filosofie MTB Daemona je taková, že veškeré operace se provádějí skrze jeho síťové
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
