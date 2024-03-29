---
layout: page
title: MTB v KMŽ Brno I
permalink: /cz/kmzbrnoI
order: 10
lang: cz
ref: kmzbrnoI
---

V [KMŽ Brno I](https://kmz-brno.cz/) jsme se rozhodli používat systém MTB už
v roce 2000. V té době jsme neměli žádné zkušenosti s použitím podobného
řídícího systému a tak jsme se rozhodli, že si to trošku odzkoušíme.

Výchozími bloky tehdy byla jedna deska MTB-UNI v1 a řídící deska MTB-PC. Po
následných pokusech a drobných odladěních jsme měli naprogramovány a odzkoušeny
jednoduché aplikace na autobloku. Výsledky byly natolik dobré, že jsme se
rozhodli podporovat tento systém do budoucnosti. Na základě našich požadavků
vznikly nové moduly [MTB-UNI](/cz/v2/uni), [MTB-TTL](/cz/v2/ttl), [MTB-REG](/cz/v2/reg),
[MTB-POT](/cz/v2/pot) a [S-com](https://www.mtb-model.com/elektro/s-com.htm). Tímto
bych chtěli poděkovat autorovi celého projektu MTB Víťovi Báňovi za ochotu
a čas strávený při vývoji systému.

Ještě v původních prostorách na Bratislavské ulici se nám podařilo postavit
jednodušší kolejiště složené z modulů, které bylo vystaveno později na zámku
v Nesovicích. Na tomto kolejišti jsme plně aplikovali systém MTB, neboť jsme
potřebovali, aby kolejiště bylo provozní co nejvíce automaticky. Na tomto
projektu jsme si systém dostatečně odzkoušeli a ověřili jeho spolehlivost
a doladili slabá místa.

Po přestěhování do nových prostor areálu bývalé Mosilany jsme se pustili do
rekonstrukce celého kolejiště a tím pádem i celé elektroniky. Dlouho jsme se
rozhodovali, zda zůstaneme u analogového řízení lokomotiv nebo se pustíme do
digitálního řízení. Po několika pokusech s analogem a zvýšenými požadavky na
ovládání lokomotiv jsme se nakonec rozhodli pro digitální řízení lokomotiv
a pořídili jsme si centrálu Intelibox. Její výhoda pro nás spočívala v tom, že
má v sobě již zabudované sériové rozhraní pro komunikaci s PC a lze využít její
sběrnici LocoNet pro připojení ovladačů a zesilovačů. Systém MTB se pro nás tak
stal základem pro celý zabezpečovací systém kolejiště, který je schopen sbírat
informace z kolejiště (detektory obsazení, IR snímače pro brzdění vlaku, polohy
přestavníků atd.) a také ovládat jednotlivé prvky (přestavníky, návěstidla,
závory atd.). Veškerá přijatá data lze zpracovat v PC a na základě jejich
vyhodnocení ovládat jednotlivé prvky kolejiště a posílat příkazy pro řízení
lokomotiv do centrály, která se tak stará o jejich provoz. Obrovská výhoda
systému MTB je pro nás v tom, že si ho můžeme dále vylepšovat podle svých
potřeb a zanedbatelná není ani výhodná cena jednotlivých modulů oproti
komerčním produktům.

Naše kolejiště je poměrně složitý projekt a tak vznikly nové požadavky na jeho
ovládání. V současné době je pro ovládání každé nové stanice používáno
samostatné PC, které nahrazuje původní ovládací panel. Tak vznikl požadavek na
síťové propojení počítačů. Zde byl největší kámen úrazu. Původní řídící program
byl koncipován pro operační systém DOS a nebylo v našich silách v něm rozchodit
síťovou komunikaci. Tudíž nezbývalo nic jiného, než celý systém přesunout pod
operační systém Windows. Uvažován byl i Linux, ale nenašel se nikdo dostupný,
kdo by s ním uměl pracovat na programátorské úrovni. Tím samozřejmě vznikl
další problém – rozhraní mezi PC a sběrnicí MTB. [Původní deska
MTB-PC](/cz/v2/isa) byla navržena pro slot ISA, který již není v novějších PC
k dispozici.

Jako komunikační port bylo tedy zvoleno rozhraní USB a k němu přes obvod
FT245BM připojen procesor 89S8252.

Takto vznikl první prototyp modulu [MTB-USB](/cz/v2/usb) v1. Jeho hlavní nevýhodou bylo že
šlo využívat pouze malou vnitřní RAM procesoru a tak nebylo příliš prostoru na
jeho rozšířené využití, ale i tak tento prototyp splnil svůj účel a byl schopen
spolehlivě komunikovat s téměř 30 připojenými moduly [MTB-UNI](/cz/v2/uni) a
[MTB-TTL](/cz/v2/ttl) a to dokonce se zvýšenou rychlostí sběrnice MTB na 115 kBaud
(původně 38 kBaud).

Jelikož vyvstal požadavek doplnit do rozhraní i určitou vlastní inteligenci
a také podporu pro moduly [MTB-REG](/cz/v2/reg) a [MTB-POT](/cz/v2/pot), vznikla
novější verze modulu [MTB-USB](/cz/v2/usb), který navíc obsahuje i paměť RAM 32kB
a je opatřen novějším obvodem USB rozhraní FT245RL. Procesor lze použít 89C52
nebo lepší.

V letech 2020 a 2021 jsme se dostali do situace, kdy staré moduly už
zastarávaly, některé součástky nebyly k sehnání a z KMŽ odešel hlavní klubovní
architekt systému MTB Petr Trávník. Rozhodli jsme se tak navrhnout nový systém
MTB, který bude otevřený a který splní všechny naše nové požadavky. Vyvstal
například požadavek na řízení jedné sběrnice pomocí více řídících systémů
(např. řízení provozu kolejiště a řízení pouličního osvětlení). Vzniklo tak
*MTB v4*.  Vznikl [nový protokol MTBbus](/cz/v4/bus), moduly MTB-UNI MTB-UNIm
a MTB-TTL byly sjednoceny do nového modulu [MTB-UNI v4](/cz/v4/uni), vznikla [deska
pro podporu IR čidel](/cz/irdet), vznikl [nový modul MTB-USB](/cz/v4/usb). Vznikly
[nové počítačové aplikace a knihovny pro přístup k MTB](/cz/v4/daemon). Autorem
MTB v4 je Jan Horáček, některé komponenty vznikaly ve spolupráci s [Laboratoří
řízení kolejových vozidel MENDELU](https://lrkv.pef.mendelu.cz/).
Tvorbu systému MTB v4 popisuje [diplomová práce](https://is.muni.cz/th/cd3ln/).
