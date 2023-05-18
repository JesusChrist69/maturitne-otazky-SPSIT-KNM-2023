# 6. Základy sietí
typy sietí, typ klient/server a peer to peer, fyzická a logická topológia, konvergovaná sieť, komponenty sietí, LAN a WAN siete, komponenty sietí z ekonomického hľadiska, podsiete pomocou VLSM a bez VLSM, OS Cisco IOS, konfigurácia smerovača a prepínača

- **LAN (Local Area Network)**: Je to súkromná sieť, ktorá pokrýva malú geografickú oblasť, ako je domácnosť, kancelária alebo škola
- **WLAN (Wireless Local Area Network)**: Je to bezdrôtová verzia LAN, ktorá používa bezdrôtové technológie, ako je Wi-Fi, na pripojenie zariadení k sieti
- **WAN (Wide Area Network)**: Je to sieť, ktorá pokrýva väčšie geografické územia, ako sú mesto, štát alebo dokonca viacero krajín.
- **MAN (Metropolitan Area Network)**: Je to sieť, ktorá pokrýva väčšiu geografickú oblasť ako LAN, ale menšiu ako WAN. MAN je obvykle implementovaná v rámci jedného mesta alebo regiónu a poskytuje vysokorýchlostné pripojenie pre verejné inštitúcie, univerzity a podobné organizácie.
- **PAN (Personal Area Network)**: Je to osobná sieť, ktorá sa vzťahuje na zariadenia, ktoré sú v bezprostrednej blízkosti jednej osoby

- Dva základné typy sieťových architektúr sú klient/server a peer-to-peer (P2P). Tu je vysvetlenie oboch typov:
  - **Klient/server**: V klient/server architektúre existuje centralizovaný server, ktorý poskytuje služby a zdroje klientom v sieti. Klienti sú zariadenia, ako sú počítače, telefóny alebo tablety, ktoré žiadajú o prístup k týmto službám a zdrojom. Server je silnejší a zdrojovo bohatší systém, ktorý zabezpečuje poskytovanie týchto služieb. Klienti komunikujú so serverom prostredníctvom siete a žiadajú o zdroje, ako sú súbory, tlačiarne, databázy alebo webové stránky. Server spravuje tieto žiadosti a poskytuje odpovede a výsledky klientom. Klient/server architektúra je bežná vo firemných sieťach, kde sa využívajú centrálne servery na správu zdrojov a zabezpečenie centrálneho riadenia a kontroly.

  - **Peer-to-peer (P2P)**: V peer-to-peer architektúre sú zariadenia (uzly) v sieti rovnocenné a komunikujú priamo medzi sebou bez centrálneho servera. Každý uzol môže fungovať ako klient aj ako server a zdieľať svoje zdroje a služby s ostatnými uzlami v sieti. V P2P sieti môžu uzly pristupovať k súborom, tlačiarňam, aplikáciám alebo iným zdrojom bez nutnosti centrálneho sprostredkovania. Peer-to-peer architektúra je často využívaná v súborovom zdieľaní, kde jednotliví používatelia zdieľajú svoje súbory s ostatnými používateľmi. Tento typ architektúry umožňuje distribuovanú a decentralizovanú výmenu dát a zdrojov medzi uzlami v sieti.

- **Fyzická topológia**: Fyzická topológia sa vzťahuje na fyzické usporiadanie a pripojenie zariadení v počítačovej sieti. Tento pojem opisuje, ako sú počítače, smerovače, prepínače a ďalšie sieťové zariadenia fyzicky pripojené a umiestnené v sieti. Fyzická topológia môže mať rôzne formy, ako sú hviezdicová topológia, kruhová topológia, zbernicová topológia, stromová topológia, mriežková topológia a podobne. Každá topológia má svoje vlastné výhody a nevýhody vzhľadom na spoľahlivosť, rozširiteľnosť, náklady na káble a ďalšie faktory.

- **Logická topológia**: Logická topológia sa vzťahuje na spôsob, akým sa dáta prenášajú a komunikujú v rámci počítačovej siete. Tento pojem opisuje vzájomné vzťahy a komunikáciu medzi sieťovými zariadeniami. Logická topológia nie je viazaná na fyzickú konektivitu a môže byť iná ako fyzická topológia siete. Najbežnejšou formou logických topológii je broadcastová topológia a point-to-point topológia. V broadcastovej topológii je komunikácia vytvorená tak, že sa dáta odosielajú na všetky zariadenia v sieti, kde si každé zariadenie vyberie, či dáta prijme alebo nie. V point-to-point topológii je komunikácia vytvorená priamo medzi dvoma koncovými zariadeniami.

- **Konvergovaná sieť** (tiež známa ako konvergovaná sieťová infraštruktúra) je sieťová architektúra, ktorá integruje viacero typov komunikačných služieb a technológií do jednej siete. Tieto služby a technológie môžu zahŕňať hlasovú komunikáciu, dátové prenosy, videohovory, správu sietí, bezpečnosť a ďalšie. Konvergovaná sieť má za cieľ zjednodušiť a zladiť správu a prevádzku rôznych komunikačných služieb v rámci jednej infraštruktúry. Namiesto oddelených sietí pre hlas, dáta a video integruje konvergovaná sieť tieto služby na jednom spoločnom prenosovom médiu a využíva spoločné sieťové prvky, ako sú smerovače a prepínače.

- **E-mailové servery**: Spravujú elektronickú poštu.
- **Web server**: Umožňuje prístup k webovým stránkam cez HTTP protokol.
- **DNS (Domain Name System) servery**: Prekladajú doménové mená na IP adresy.
- **DHCP (Dynamic Host Configuration Protocol) servery**: Automaticky prideľujú IP adresy zariadeniam v sieti.

- **Cisco IOS (Internetwork Operating System)** je operačný systém vyvinutý spoločnosťou Cisco pre sieťové zariadenia, ako sú smerovače, prepínače a firewall-y. Je to komplexný a robustný operačný systém, ktorý poskytuje množstvo funkcií a nástrojov pre správu, konfiguráciu a prevádzku sieťových zariadení.

### Zariadenia siete
- **Smerovače (routery)**: Smerujú pakety dát medzi rôznymi sieťami a rozhodujú o optimálnych cestách prenosu.
- **Prepínače (switches)**: Umožňujú prepojenie zariadení v rámci lokálnej siete (LAN) a spravujú tok dát medzi nimi.
- **Koncentrátory (hubs)**: Slúžia na zdieľanie siete a rozširovanie signálu na viacero portov.

### Káblové média
- **Twisted Pair káble**: Kategória 5e (Cat 5e) a novšie káble sa často používajú pre Ethernetové pripojenia v LAN sieťach.
- **Koaxiálne káble**: Používané pre sietí typu Cable TV alebo pre pripojenie starších typov sietí.
- **Optické vlákna**: Poskytujú vysokú rýchlosť a výkonnosť pre dlhé vzdialenosti a sú bežné vo WAN sieťach.

### Aktívne prvky
- **Sieťové karty (Network Interface Cards - NICs)**: Pripájajú počítače a iné zariadenia k sieti.
- **Access Points (APs)**: Poskytujú bezdrôtové pripojenie do WLAN sietí.
- **Modemy**: Prekladajú digitálne signály na analógové (a naopak) pre pripojenie k internetu cez telefónne alebo káblové linky.
- **Firewall**: Zabezpečuje ochranu siete pred neoprávneným prístupom a monitoruje sieťovú komunikáciu.


### Protokoly:
- **IP (Internet Protocol)**: Zabezpečuje adresovanie a smerovanie dát v sieti.
- **TCP (Transmission Control Protocol)**: Poskytuje spoľahlivú prenosovú vrstvu, ktorá zabezpečuje doručenie dát bez straty alebo duplikácie.
- **UDP (User Datagram Protocol)**: Poskytuje jednoduchú prenosovú vrstvu bez spoľahlivosti, čo je vhodné pre niektoré aplikácie, kde je vyšší dôraz na rýchlosť.
- **Sieťové aplikácie a služby**:

### VLSM
- **Bez VLSM**:
  - Bez použitia VLSM sa celá sieť delí na podsiete s rovnakou maskou podsiete. To znamená, že všetky podsiete majú rovnaký počet hostiteľov a rovnaký rozsah adries. Táto metóda je jednoduchá, ale môže viesť k plytvaniu IP adries, pretože každá podsieť musí mať dostatočný počet adries aj v prípade, že reálne nepotrebuje všetky tieto adresy.

- **S VLSM**:
  - VLSM umožňuje pridelenie rôznych veľkostí podsietí v rámci jednej siete, čo znamená, že každá podsieť môže mať odlišný počet hostiteľov a rozsah adries. Týmto spôsobom je možné efektívne využiť IP adresy a minimalizovať ich plytvanie. S použitím VLSM je možné prideliť menšie podsiete tam, kde je potrebný menší počet hostiteľov, a väčšie podsiete tam, kde je potrebný väčší počet hostiteľov.

Konfigurácia smerovača:
1.	Prihláste sa do smerovača cez konzolu alebo vzdialene.
2.	Prepnite sa do privilegového módu príkazom enable.
3.	Prejdite do konfiguračného módu príkazom configure terminal.
4.	Nastavte názov smerovača príkazom hostname.
5.	Nastavte heslo pre prístup k privilegovanému módu príkazom enable secret.
6.	Nastavte heslo pre vzdialený prístup k smerovaču príkazom line vty a password.
7.	Nastavte rozhranie smerovača príkazom interface a nastavte IP adresu a masku siete.
8.	Ak je potrebné, nastavte statické smerovanie príkazom ip route.

### Konfigurácia prepínača
- Prihláste sa do prepínača cez konzolu alebo vzdialene.
- Prepnite sa do privilegového módu príkazom enable.
- Prejdite do konfiguračného módu príkazom configure terminal.
- Nastavte názov prepínača príkazom hostname.
- Nastavte heslo pre prístup k privilegovanému módu príkazom enable secret.
- Nastavte heslo pre vzdialený prístup k prepínaču príkazom line vty a password.
- Nastavte rozhranie prepínača príkazom interface a nastavte IP adresu a masku siete.
- Nastavte režim rozhrania (access, trunk, dynamic) príkazom switchport mode.
- Ak je potrebné, nastavte VLAN príkazom vlan.


[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
