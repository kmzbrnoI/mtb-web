---
layout: page
title: MTB Daemon
permalink: /cz/v4/daemon
order: 51
lang: cz
ref: daemon
---

*MTB Daemon* je počítačová konzolová aplikace, která umožňuje propojení
[MTB-USB](usb) s řídicími softwary kolejiště. Uchovává konfiguraci MTB modulů.
K aplikaci se může připojit více programů řídících provoz, například software
zabezpečující řízení jízdy vlaků, software řešící osvětlení, software řešící
tramvajovou dopravu apod.

Řídicí programy se připojují přes TCP spojení, lze je tedy umístit i na jiný
počítač.

 * [Specifikace protokolu pro připojení klientů](https://github.com/kmzbrnoI/mtb-daemon/tree/master/tcp-protocol)
 * [Zdrojové kódy MTB Daemon](https://github.com/kmzbrnoI/mtb-daemon)
 * [Stáhnout MTB Daemon](https://github.com/kmzbrnoI/mtb-daemon/releases)

Celková architektura použití systému MTB pak může vypadat například takto:

<figure>
<img src="/assets/img/mtbv4-topology.svg" alt="Topologie sběrnice MTBbus" style="width: 100%; max-width: 600px" />
<figcaption>Topologie sběrnice MTBbus.</figcaption>
</figure>

*hJOP* je software řídící provoz kolejiště. *MTB Net Lib* je knihovna propojující
*hJOP* a *MTB Daemon*, ke stažení [zde](https://github.com/kmzbrnoI/mtb-net-lib).
