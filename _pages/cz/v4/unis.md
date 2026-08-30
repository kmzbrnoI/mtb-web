---
layout: page
title: Modul MTB-UNIS
permalink: /cz/v4/unis
lang: cz
order: 24
ref: unis
---

Modul MTB-UNIS umožňuje připojení digitálních vstupů, digitálních výstupů,
S-com výstupů a serv. Autorem modulu je Ing. Michal Petrilak.

<figure>
<img src="/assets/img/mtb4/mtb-unis-photo.jpg" alt="Modul MTB-UNIS" style="width: 100%; max-width: 500px" />
<figcaption>Modul MTB-UNIS</figcaption>
</figure>

 * Počet vstupů: 16 (připojení TTL signálů, spínacích kontaktů nebo otevřených kolektorů).
 * Počet výstupů: 16 spínacích tranzistorů, tj. 8 dvoučinných přestavníků.
 * Počet serv: 6.
 * Ovládaní až 16 návěstidel vybavených rozhraním
   [S-com](https://www.mtb-model.com/elektro/s-com.htm).
 * Kmitání výstupů.
 * Napájení: 7–17 V DC.

Budiče výstupů můžou spínat zátěž 28V/0.5A pomocí tranzistoru NPN
s otevřeným kolektorem. Vstupní obvody jsou navrženy univerzálně pro připojení
binárních signálů (kontakty relé, TTL, aj.). Vstupy obsahují *pull-up* rezistory.

Srdcem modulu je procesor ATmega128a, který obsahuje všechny potřebné funkce
pro řízení a komunikaci. Připojení signálů je realizováno pomocí svorkovnic,
rozhraní MTBbus se připojuje také svorkovnicemi.

* [Firmware](https://github.com/petrilakm/mtb-unis-fw)

## Konfigurace modulu

<figure>
<img src="/assets/img/mtb4/mtb-unis-config.png" alt="Konfigurace modulu MTB-UNIS" style="height: 100%" />
<figcaption>Konfigurace modulu MTB-UNIS</figcaption>
</figure>

## Stav modulu

<figure>
<img src="/assets/img/mtb4/mtb-unis-io.png" alt="Stav modulu MTB-UNIS" style="height: 100%" />
<figcaption>Stav modulu MTB-UNIS. Zobrazuje se stav vstupů, výstupů a koncových poloh serv. Lze nastavit výstupy a polohovat serva. Lze ladit přesné polohy serv.</figcaption>
</figure>

<!-- <figure>
<img src="/assets/img/mtb4/uni-v40-psh-all.jpg" alt="Modul MTB-UNI v4.0" style="width: 100%; max-width: 500px" />
<figcaption>Modul MTB-UNI v4.0 se zásuvnými konektory</figcaption>
</figure> -->

<!-- <div style="text-align:center;">
<a class="btn" style="width:200px; margin: 10px;" href="uni-manual">Návod k použití</a>
<a class="btn" style="width:200px; margin: 10px;" href="/cz/poridit">Chci si pořídit MTB-UNI v4</a>
</div> -->
