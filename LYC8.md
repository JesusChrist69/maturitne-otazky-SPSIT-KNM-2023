# 8. Smerovanie a smerovače
sieťová vrstva, smerovanie v počítačových sieťach, statické a dynamické smerovanie, smerovacia tabuľka, brána, metrika cesty, administratívna vzdialenosť, konvergentnosť siete, štandardná cesta, autonómny systém, vnútorné a vonkajšie smerovacie protokoly, protokoly vektora vzdialenosti a stavu linky, IPv6 smerovacie protokoly, smerovač, jeho časti, funkcie a vlastnosti, typy pamätí smerovača, prístupové metódy na konfiguráciu smerovača

- **Sieťová vrstva** je jednou z vrstiev v modeli ISO/OSI (Open Systems Interconnection) a TCP/IP (Transmission Control Protocol/Internet Protocol). Je to vrstva, ktorá sa zaoberá prenosom dát medzi rôznymi sieťovými zariadeniami v rámci siete.
- **Smerovanie v počítačových sieťach** je proces, ktorý sa zaoberá rozhodovaním, akou cestou majú byť pakety dát prenášané medzi sieťovými zariadeniami. Jeho úlohou je nájsť optimálnu cestu pre prenos dát z jedného uzla na druhý v rámci siete.
  - Pri smerovaní sa využívajú rôzne smerovacie protokoly, ktoré určujú, ako sa rozhoduje o optimálnych cestách a ako sa smerovače a sieťové uzly informujú o sieti a dostupných cestách.
   - 1.	Statické smerovanie:
    -	Pri statickom smerovaní sú smerovacie tabuľky nastavené manuálne administrátorom siete.
    -	Administrátor musí ručne definovať cesty a smerovacie vstupy pre rôzne siete a smerovače.
    -	Statické smerovanie je jednoduché a ľahké na implementáciu a konfiguráciu.
    -	Je vhodné pre jednoduché siete s malým počtom uzlov, kde sa topológia siete zriedka mení.
   - 2.	Dynamické smerovanie:
    -	Pri dynamickom smerovaní smerovače používajú smerovacie protokoly na výmenu informácií o topológii siete a automaticky sa rozhodujú o optimálnych cestách.
    -	Smerovacie protokoly ako napríklad OSPF (Open Shortest Path First), EIGRP (Enhanced Interior Gateway Routing Protocol) alebo BGP (Border Gateway Protocol) sú bežne používané pre dynamické smerovanie.
    -	Dynamické smerovanie je flexibilnejšie a môže sa prispôsobovať zmenám v topológii siete.
    -	Je vhodné pre rozsiahle siete s veľkým počtom uzlov a v prípadoch, keď sa topológia siete často mení.

- **Smerovacia tabuľka** je dôležitým prvkom pri rozhodovaní o tom, ako smerovač prenáša pakety dát v počítačovej sieti. Je to tabuľka, ktorá obsahuje informácie o dostupných sieťach a cestách, ktoré smerovač používa na rozhodovanie o tom, kam preposlať paket na základe jeho cieľovej adresy.
- **Brána smerovania (gateway)** je sieťové zariadenie, ktoré slúži na prenos paketov medzi rôznymi sieťami s rôznymi adresnými rozsahmi. Funguje ako rozhranie medzi dvoma sieťami, čo umožňuje prenos dát medzi nimi.
- **Metrika cesty** je hodnota alebo metrika, ktorá sa používa pri rozhodovaní o optimálnosti cesty pri smerovaní paketov v počítačových sieťach. Metrika poskytuje informáciu o kvalite a výkonnosti danej cesty a pomáha určiť najlepšiu cestu, ktorou majú byť pakety prenesené.
- **Administratívna vzdialenosť (administrative distance)** je koncept, ktorý sa používa pri rozhodovaní o výbere najlepšej cesty medzi rôznymi smerovačmi alebo smerovacími protokolmi v počítačových sieťach. Každý smerovač alebo smerovací protokol má priradenú administratívnu vzdialenosť, ktorá predstavuje preferenciu alebo dôveru v daný smerovač alebo protokol.
- **Konvergentnosť siete** sa vzťahuje na schopnosť siete obnoviť sa po výpadku alebo zlyhaní tak, aby sa obnovila normálna prevádzka a dostupnosť služieb. Je to kritická vlastnosť pre počítačové siete, ktorá zabezpečuje, že sieť môže fungovať spoľahlivo aj v prípade chýb, porúch alebo iných udalostí.
- V kontexte smerovania v počítačových sieťach sa "**štandardná cesta**" (default route) vzťahuje na predvolenú cestu, ktorou sa preposielajú pakety, ak nie je špecifikovaná žiadna konkrétna cieľová sieť v smerovacej tabuľke.

### Autonómny systém (AS)
- **Autonómny systém (AS)** je súbor smerovačov a sietí, ktoré sú pod spoločnou správou a kontrolou. AS je základnou jednotkou smerovania v protokole BGP (Border Gateway Protocol) používanom na smerovanie na internete.
- Každý autonómny systém je priradený unikátny identifikátor (AS číslo), ktorý ho jednoznačne identifikuje v rámci celého internetu. 
- Vnútorné a vonkajšie smerovacie protokoly sú dva typy protokolov, ktoré sa používajú pri smerovaní paketov v počítačových sieťach:
   - 1. **Vnútorné smerovacie protokoly (Interior Gateway Protocols - IGP)**:
    -	Vnútorné smerovacie protokoly sa používajú v rámci jedného autonómneho systému (AS) alebo vnútri jednej organizácie.
    -	Slúžia na smerovanie paketov medzi smerovačmi v rámci jednej siete a na výmenu smerovacích informácií medzi smerovačmi v rámci toho istého AS.
    -	Bežne používané vnútorné smerovacie protokoly zahŕňajú Routing Information Protocol (RIP), Open Shortest Path First (OSPF) a Intermediate System to Intermediate System (IS-IS).
    -	Cieľom vnútorných smerovacích protokolov je nájsť najlepšiu cestu medzi susednými smerovačmi v rámci jedného AS a optimalizovať smerovaciu tabuľku v rámci tejto siete.
   - 2. **Vonkajšie smerovacie protokoly (Exterior Gateway Protocols - EGP)**:
    -	Vonkajšie smerovacie protokoly sa používajú na smerovanie medzi rôznymi autonómnymi systémami (AS) alebo medzi rôznymi poskytovateľmi internetových služieb.
    -	Tieto protokoly slúžia na výmenu smerovacích informácií medzi smerovačmi rôznych AS a umožňujú smerovanie paketov medzi rôznymi sieťami a poskytovateľmi.
    -	Najznámejším vonkajším smerovacím protokolom je Border Gateway Protocol (BGP), ktorý sa používa na smerovanie na internete medzi rôznymi ISP a AS.
    -	Vonkajšie smerovacie protokoly majú väčšiu komplexitu a môžu zahŕňať rôzne kritériá rozhodovania o cestách vrátane politík, prepúšťania a filtrovania smerovania.

- **Vnútorné a vonkajšie smerovacie protokoly** spolu spolupracujú a umožňujú efektívne a spoľahlivé smerovanie paketov v rámci sietí a medzi rôznymi sieťami a autonómnymi systémami.

- **Protokoly vektora vzdialenosti (distance-vector protocols)** a protokoly stavu linky (link-state protocols) sú dva základné typy smerovacích protokolov používaných v počítačových sieťach. Tieto protokoly sa líšia v spôsobe, ako sa smerovacie informácie vymieňajú a ako sa rozhoduje o najlepších cestách pre prenos paketov. Protokoly vektora vzdialenosti (distance-vector protocols) a protokoly stavu linky (link-state protocols) sú dva základné typy smerovacích protokolov používaných v počítačových sieťach. Tieto protokoly sa líšia v spôsobe, ako sa smerovacie informácie vymieňajú a ako sa rozhoduje o najlepších cestách pre prenos paketov.
  - 1. **Protokoly vektora vzdialenosti**:
   -	Protokoly vektora vzdialenosti používajú jednoduchú metriku (často založenú na počte skokov alebo metrických jednotkách) na určenie najlepšej cesty k cieľovej sieti.
   -	Každý smerovač vysiela svoju smerovaciu tabuľku susedným smerovačom, ktorí vymieňajú tieto informácie s ďalšími smerovačmi v sieti.
   -	Smerovače sa navzájom informujú o svojich dostupných cestách a aktualizujú svoje smerovacie tabuľky v závislosti od týchto informácií.
   -	Bežné protokoly vektora vzdialenosti zahŕňajú Routing Information Protocol (RIP) a Interior Gateway Routing Protocol (IGRP).
  - 2. **Protokoly stavu linky**:
   -	Protokoly stavu linky používajú podrobnejšie informácie o topológii siete a stavu jednotlivých linkov na výpočet najlepších ciest.
   -	Každý smerovač zhromažďuje informácie o všetkých smerovačoch v sieti a stavu ich linky.
   -	Tieto informácie sa distribuujú medzi všetkými smerovačmi v sieti, čím sa vytvorí graf topológie siete.
   -	Smerovače využívajú algoritmus (často Dijkstraov algoritmus) na výpočet najkratších ciest a najlepších ciest na základe tejto topológie.
   -	Bežné protokoly stavu linky zahŕňajú Open Shortest Path First (OSPF) a Intermediate System to Intermediate System (IS-IS).

- Niektoré z týchto smerovacích protokolov, ktoré sú používané v prostredí **IPv6**, sú:
1.	OSPFv3 (Open Shortest Path First version 3): Je verzia protokolu OSPF pre IPv6. Podobne ako OSPF pre IPv4, OSPFv3 je protokol stavu linky, ktorý vymieňa informácie o topológii siete medzi smerovačmi. OSPFv3 umožňuje smerovanie IPv6 paketov a je široko používaný v prostredí IPv6.
2.	RIPng (Routing Information Protocol next generation): RIPng je verzia protokolu RIP pre IPv6. RIPng je protokol vektora vzdialenosti, ktorý vymieňa smerovacie informácie medzi smerovačmi. Podobne ako RIP pre IPv4, RIPng má jednoduchú metriku (hop count) a je jednoduchý na konfiguráciu.
3.	IS-IS (Intermediate System to Intermediate System): IS-IS je smerovací protokol, ktorý je nezávislý na konkrétnej verzii IP (IPv4 alebo IPv6). Pre IPv6 sa používa rovnaká verzia protokolu IS-IS ako pre IPv4. IS-IS je protokol stavu linky, ktorý vymieňa informácie o topológii siete medzi smerovačmi.
4.	BGP (Border Gateway Protocol): BGP je vonkajší smerovací protokol, ktorý sa používa na smerovanie medzi rôznymi autonómnymi systémami (AS). Pre IPv6 sa používa rovnaká verzia protokolu BGP ako pre IPv4. BGP je široko používaný na internete pre smerovanie IPv6 paketov medzi rôznymi poskytovateľmi internetových služieb.

- **Smerovač (router)** je sieťové zariadenie, ktoré slúži na prenos paketov medzi rôznymi sieťami na základe informácií v smerovacej tabuľke. Jeho hlavnou funkciou je rozhodovať o správnom smere prenosu paketov z jednej siete do druhej, aby dosiahli svoj cieľový sieťový segment.

- **Smerovač sa skladá z niekoľkých základných častí**, ktoré spolupracujú na správe a prenose dát v sieti. Tu je základný prehľad niektorých hlavných častí smerovača:
1.	Sieťové rozhrania: Smerovač má jedno alebo viacero fyzických alebo logických rozhraní, ktoré sú pripojené k rôznym sieťovým segmentom. Tieto rozhrania slúžia na komunikáciu so zariadeniami v týchto sieťach a umožňujú príjem a odosielanie paketov.
2.	Smerovacia tabuľka: Smerovacia tabuľka je dôležitou súčasťou smerovača. Obsahuje informácie o dostupných sieťach a najlepších cestách k týmto sieťam. Smerovač používa tieto informácie na rozhodovanie o tom, kam smerovať pakety na základe ich cieľovej IP adresy.
3.	Smerovací procesor: Smerovací procesor je zodpovedný za spracovanie paketov a vykonávanie smerovacích funkcií. Tento procesor vykonáva rôzne algoritmy na analýzu paketov, konzultáciu smerovacej tabuľky a rozhodovanie o tom, kam smerovať pakety.
4.	Správa prenosu: Ďalšou dôležitou časťou smerovača je správa prenosu (switching fabric), ktorá sa stará o presmerovanie paketov medzi vstupnými a výstupnými rozhraniami. Správa prenosu zabezpečuje rýchly a efektívny prenos paketov medzi rôznymi sieťovými rozhraniami smerovača.
5.	Protokoly smerovania: Smerovač podporuje rôzne smerovacie protokoly (ako sme spomínali v predchádzajúcej odpovedi), ktoré umožňujú výmenu smerovacích informácií medzi smerovačmi v sieti. Tieto protokoly zabezpečujú aktualizácie smerovacej tabuľky a správne smerovanie paketov v sieti.
6.	Správa a konfigurácia: Smerovač tiež obsahuje funkcie na správu a konfiguráciu. To zahŕňa možnosť nastavenia rôznych parametrov smerovania, monitorovania prevádzky siete, diagnostiky problémov a aktualizácie firmvéru smerovača.

- **Smerovač má viaceré funkcie**, ktoré zabezpečujú správne fungovanie siete a smerovanie paketov. Tu je prehľad niektorých hlavných funkcií smerovača:
1.	Smerovanie paketov: Hlavnou funkciou smerovača je smerovať pakety medzi rôznymi sieťami na základe ich cieľovej IP adresy. Smerovač používa smerovaciu tabuľku na rozhodnutie o optimálnej trase pre pakety.
2.	Smerovacia tabuľka: Smerovač udržiava smerovaciu tabuľku, ktorá obsahuje informácie o dostupných sieťach a ich príslušných rozhraniach. Tieto informácie sú využívané na rozhodovanie o smerovaní paketov.
3.	Protokoly smerovania: Smerovač podporuje rôzne smerovacie protokoly, ako OSPF (Open Shortest Path First), RIP (Routing Information Protocol), BGP (Border Gateway Protocol) atď. Tieto protokoly slúžia na výmenu smerovacích informácií medzi smerovačmi a aktualizáciu smerovacej tabuľky.
4.	Filtrovanie paketov: Smerovač môže filtrovať prichádzajúce a odchádzajúce pakety na základe rôznych kritérií, ako sú zdrojová a cieľová IP adresa, porty, protokoly atď. Toto umožňuje implementáciu bezpečnostných politík a obmedzenie prístupu do siete.
5.	Network Address Translation (NAT): Smerovač môže podporovať NAT, čo umožňuje prekladanie IP adries medzi privátnymi (vnútornými) a verejnými (vonkajšími) sieťovými rozhraniami. To umožňuje viacerým zariadeniam súkromnej siete zdieľať jednu verejnú IP adresu.
6.	Bezpečnosť siete: Smerovač môže poskytovať rôzne bezpečnostné funkcie, ako je firewall, VPN (Virtual Private Network), IPSec (Internet Protocol Security), ochrana pred DoS útokmi (Denial of Service) a iné mechanizmy na ochranu siete a jej prevádzky.

- **Smerovač má niekoľko vlastností**, ktoré ho odlišujú od iných sieťových zariadení. Tu sú niektoré z hlavných vlastností smerovača:
1.	Smerovanie na základe IP adresy: Smerovač smeruje pakety na základe ich cieľovej IP adresy. Používa smerovaciu tabuľku na rozhodnutie o optimálnej trase pre pakety.
2.	Rozhodovanie o najlepšej ceste: Smerovač rozhoduje o najlepšej ceste, ktorou by sa mal paket poslať na základe rôznych faktorov, ako je dĺžka trasy, priepustnosť, oneskorenie, kvalita služby (QoS) a iné parametre.
3.	Smerovacia tabuľka: Smerovač udržiava smerovaciu tabuľku, ktorá obsahuje informácie o dostupných sieťach a ich príslušných rozhraniach. Tieto informácie sa používajú na rozhodovanie o smerovaní paketov.
4.	Podpora rôznych smerovacích protokolov: Smerovač podporuje rôzne smerovacie protokoly, ako OSPF, RIP, BGP, ISIS, ktoré umožňujú výmenu smerovacích informácií medzi smerovačmi a aktualizáciu smerovacej tabuľky.

- **Smerovač obsahuje viacero typov pamätí** na ukladanie rôznych informácií potrebných pre jeho fungovanie:
1.	Tabuľka smerovania: obsahuje informácie o sietiach a najlepšej ceste k nim. Táto tabuľka sa aktualizuje pomocou smerovacích protokolov.
2.	Cache pamäť: uchováva informácie o nedávno použitých cestách, aby sa zrýchli proces smerovania a zníži sa záťaž smerovača.
3.	ARP cache: uchováva mapovanie IP adries na MAC adresy pre miestne siete, aby sa zrýchlilo doručenie paketov.
4.	Buffery: slúžia na dočasné ukladanie paketov, ktoré čakajú na odoslanie alebo spracovanie.

- **Na konfiguráciu smerovača** je možné použiť rôzne prístupové metódy, závisí to od typu smerovača a jeho konfiguračného rozhrania. Tu sú niektoré z najbežnejších prístupových metód na konfiguráciu smerovača:
1.	Konzola: Prístup cez konzolový port smerovača umožňuje priamy prístup k jeho konfigurácii pomocou sériového rozhrania. Po pripojení k smerovaču cez konzolu je možné cez terminálový program (napríklad HyperTerminal) vstupovať príkazy a konfigurovať smerovač.
2.	Telnet: Ak smerovač podporuje protokol Telnet, je možné sa k nemu pripojiť cez sieťové rozhranie. Používateľ môže pomocou terminálového programu (napríklad PuTTY) pristupovať k smerovaču a konfigurovať ho cez príkazový riadok.
3.	SSH (Secure Shell): SSH je bezpečnejší protokol ako Telnet a umožňuje šifrovanú komunikáciu medzi konfiguračným zariadením a smerovačom. Používa sa na vzdialenú konfiguráciu smerovača cez sieť.


[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
