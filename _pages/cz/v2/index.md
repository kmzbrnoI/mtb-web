---
layout: page
title: MTB v2
permalink: /v2/index
order: 55
lang: cz
ref: mtbv2
---

MTB v2 se již v KMŽ Brno I nepoužívá. MTB v4 přinesla nový komunikační protokol
sjednotila moduly a přinesla mnohá další vylepšení. Dokumentace starého systému
MTB v2 je k dispozici zde.

* [Sběrnice MTBbus v2](bus)

## Moduly

Sběrnice MTB je řízení *master* modulem [MTB-USB](usb). Historicky byla
sběrnice řízena [zásuvnou kartou do ISA sběrnice](isa).

Ke sběrnici lze připojit tyto moduly v režimu *slave*:

 * [MTB-UNI](uni)
 * [MTB-TTL](ttl)
 * [MTB-REG](reg)
 * [MTB-POT](pot)

V počítači lze pro připojení k MTB-USB modulu použít [knihovnu](lib).
Existuje [testovací software](testsw).
