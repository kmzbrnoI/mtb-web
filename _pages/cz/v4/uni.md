---
layout: page
title: Modul MTB-UNI v4
permalink: /cz/v4/uni
lang: cz
order: 23
ref: uni
---

Modul MTB-UNI umožňuje připojení digitálních vstupů, digitálních výstupů
a S-COM výstupů. Nahrazuje moduly [MTB-UNI v2](/cz/v2/uni), [MTB-UNIm v2](/cz/v2/unim)
a [MTB-TTL v1](/cz/v2/ttl).

<figure>
<img src="/assets/img/mtb4/uni-v40-screw-all.jpg" alt="Modul MTB-UNI v4.0" style="width: 100%; max-width: 500px" />
<figcaption>Modul MTB-UNI v4.0</figcaption>
</figure>

 * Počet vstupů: 16 (připojení TTL signálů, spínacích kontaktů nebo otevřených kolektorů).
 * Počet výstupů: 16 spínacích tranzistorů, tj. 8 dvoučinných přestavníků.
 * Ovládaní až 16 návěstidel vybavených rozhraním
   [S-com](https://www.mtb-model.com/elektro/s-com.htm).
 * Kmitání výstupů.
 * Napájení: 7–17 V DC.
 * Náklady na výrobu: ~500 Kč.
 * Prodejní cena sestaveného a otestovaného kusu: 850 Kč.

Budiče výstupů můžou spínat zátěž 28V/0.5A pomocí tranzistoru NPN
s otevřeným kolektorem. Vstupní obvody jsou navrženy univerzálně pro připojení
binárních signálů (kontakty relé, TTL, aj.). Vstupy i výstupy obsahují ochranu
proti nadproudu a přepětí. Vstupy obsahují *pull-up* rezistory.

Srdcem modulu je procesor ATmega128a, který obsahuje všechny potřebné funkce
pro řízení a komunikaci. Připojení signálů je realizováno pomocí zásuvných
konektorů nebo svorkovnic (variantní osazení DPS), rozhraní MTBbus se připojuje
šroubovými svorkami.

<figure>
<img src="/assets/img/mtb4/uni-v40-psh-all.jpg" alt="Modul MTB-UNI v4.0" style="width: 100%; max-width: 500px" />
<figcaption>Modul MTB-UNI v4.0 se zásuvnými konektory</figcaption>
</figure>

Připojení IR čidel, které podporovala deska [MTB-UNI v2](/cz/v2/uni) je možné
skrze speciální desku [IR čidel](/cz/irdet).

Veškerá výrobní data modulu jsou k dispozici pod otevřenou licencí. Očekává se
automatické osazování součástek.

 * [Schéma a deska plošných spojů](https://github.com/kmzbrnoI/mtb-uni-4-ele)
 * [Firmware](https://github.com/kmzbrnoI/mtb-uni-4-fw)

Modul vznikl ve spolupráci s [Laboratoří řízení kolejových vozidel Mendelový
univerzity v Brně](https://lrkv.pef.mendelu.cz/).

<div style="text-align:center;">
<a class="btn" style="width:200px; margin: 10px;" href="uni-manual">Návod k použití</a>
<a class="btn" style="width:200px; margin: 10px;" href="/cz/poridit">Chci si pořídit MTB-UNI v4</a>
</div>
