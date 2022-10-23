---
layout: page
title: Návod k MTB-UNI v4
permalink: /cz/v4/uni-manual
lang: cz
hide: true
---

MTB-UNI v4 je univerzální modul s 16 digitálními vstupy a 16 digitálními výstupy,
který se připojuje na sběrnici MTBbus.

## Napájení, sběrnice

Modul je optimální napájet stabilizovaným napětím 12 V stejnosměrných. Modul
toleruje napájení 7–17 V stejnosměrných. Napájení se připojuje na svorky označené
"+12V" (kladný pól) a "GND" (záporný pól) na velkých svorkovnicích. Svorkovnice
jsou na desce dvě. Je jedno, na kterou svorkovnici je napájení připojeno,
svorkovnice mají propojené vodiče pro snazší instalaci.

Sběrnice *MTBbus* se připojuje do svorek "+R" a "-R". Sběrnice propojuje
všechny moduly kolejiště a *MTB-USB* modul.

Standardní odběr jednoho *MTB-UNI v4* modulu je 40 mA, maximální odběr je 100 mA.

Modul *MTB-UNI* obsahuje ochranu proti přepólování vstupního napětí (modul
nenaběhne) a proti přepětí. V případě přepětí modul přizemní napájecí vodič,
načež zareaguje vratná PTC pojistka, která přeruší přívod napájení.

## Vstupy

*MTB-UNI* podporuje 16 digitálních binárních vstupů. Vstupy jsou aktivní
v přizemněném stavu vzhledem ke GND *MTB-UNI*. To znamená, že je třeba propojit
země všech vstupních periferií a *MTB-UNI*.

Vstupy obsahují pull-rezistory k napětí +5V, takže optimální řešení výstupů
periferie připojené na vstup MTB-UNI je *otevřený kolektor*.

Vstupy obsahují ochranu proti přepětí. Jakmile napětí na vstupu přesáhne cca
5.2 V, dojde k trvalému přizemnění vstupu. Pokud externí periferie dodává stále
toto napětí, dojde k odpojení vstupu pomocí vratné PTC pojistky. Tento stav lze
rozpoznat tak, že celá osmice vstupů se jeví jako aktivní.

## Výstupy

*MTB-UNI* obsahuje 16 digitálních výstupů pracujících v režimu *otevřený
kolektor*. Maximální proud jedním výstupem je 500 mA, avšak jedná se o maximální
proud společný pro osmici výstupů. Je možné odebírat např.

* z jediného výstupu osmice 500 mA,
* ze dvou výstupů osmice po 250 mA,

ale není možné ze všech 8 výstupů kontinuálně odebírat 500 mA.

Výstupy pracují v režimu, kdy přizemněný výstup znamená aktivní výstup.
V závislosti na použitém řídicím softwaru výstupy mohou kmitat či generovat signál
[S-COM](https://www.mtb-model.com/elektro/s-com.htm) pro řízení návěstidel.

## Konfigurace adresy

Modul může mít adresu v rozsahu 1–255. Adresa se konfiguruje pomocí vložení
propojek do pozic označených na desce "1" – "128". Číslo udává desítkovou hodnotu příslušného
bitu, zasunutím propojky se bit stává aktivním.

**Pozor**: maximální počet modulů připojených ke sběrnici *MTBbus* závisí od
použitých komunikačních obvodů. Standardně se dodávají komunikační obvody
umožňující maximálně 32 modulů na sběrnici. Na žádost lze osadit obvody
umožňující až 255 modulů.

## Tlačítko

Krátké stisknutí tlačítka během provozu způsobí znovu načtení adresy.
Pokud změníte adresu během provozu, aby se změna projevila, je třeba stisknout
tlačítko.

Dlouhý stisk tlačítka přepne modul do *detekčního režimu*. Detekční režim je
indikován svítící modrou LED a slouží k detekci rychlosti *MTBbus*. *MTB-UNI* je
vždy nakonfigurováno na použití konkrétní komunikační rychlosti. Může se stát,
že po zapojení nových modulů mají tyto moduly uloženou jinou rychlost, než
kterou používá *MTBbus*. V takovém případě je možné vstoupit do *detekčního
režimu*, který postupně zkouší všechny možné rychlosti a pokouší se najít tu,
na které probíhá komunikace po *MTBbus*. Jakmile je rychlost detekována, modrá
LED zhasne a zelená LED přejde do standardního rychlého blikání.

Držení tlačítka při zapnutí napájení modulu způsobí, že modul zůstane
v *bootloaderu*. Toto je indikováno střídaným kmitáním zelené a červené LED.
Jedná se o diagnostický režim. Tento režim se opouští restartováním napájení
modulu.

## Indikační LED

Rychle blikající zelená LED indikuje standardní funkci modulu.

Pomalu blikající červená LED indikuje problém, typicky:

1. Není nakonfigurována adresa (žádná propojka nezapojena).
2. Sběrnice je špatně připojena – typicky prohozené vodiče *+R* a *-R*.

Pokud po startu střídavě kmitají červená a zelená LED, došlo k nevratné poruše
modulu, kterou je možné opravit pouze servisním zásahem u výrobce.

Svítící modrá LED indikuje aktivní *detekční dežim*, viz výše.

Blikající modrá LED indikuje aktivní rozpoznávající znak. Tuto funkci je možné
zapnout z PC, aby bylo možné pod kolejištěm snadno najít modul s konkrétní
adresou.
