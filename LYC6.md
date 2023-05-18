# 6. Základy sietí
typy sietí, typ klient/server a peer to peer, fyzická a logická topológia, konvergovaná sieť, komponenty sietí, LAN a WAN siete, komponenty sietí z ekonomického hľadiska, podsiete pomocou VLSM a bez VLSM, OS Cisco IOS, konfigurácia smerovača a prepínača

### Rozdiely medzi IPv4 a IPv6
  - IPv4 aj IPv6 sa odvolávajú na štandardy adries IP, ktoré definujú, ako sa prideľuje adresa IP a čo bude. Tu čísla, tj. 4 a 6, označujú číslo verzie.
  - IPv4 je staršia verzia, ktorej dochádzajú IP adresy na pridelenie, a IPv6 je nová verzia, ktorá bola vydaná, aby uspokojila rastúci dopyt po IP adresách.
  - Protokol IPv4 má adresy IP, ktoré sú 32-bitovými číselnými hodnotami zapísanými v desatinnom systéme, zatiaľ čo protokol IPv6 má 128 bitov zapísaných v hexadecimálnom systéme.
  - Internetový protokol verzia 6 (IPv6) je pokročilejšia a má schopnosť poskytovať nekonečný počet adries.
  - Protokol IPv4 používa štyri 1 bajtové desatinné čísla oddelené bodkou (.) A každá časť obsahuje číslo v rozsahu od o do 255 zatiaľ čo IPv6 používa hexadecimálne čísla, ktoré sú oddelené dvojbodkami a obsahujú 8 častí so 4 číslami.
  - Protokol IPv6 používa menej ako 1% sietí, zatiaľ čo protokol IPv4 sa stále používa pre zvyšných 99%.
  - Protokol IPv6 je vhodnejší pre mobilné siete ako protokol IPv4.

### IPv4
- je verzia 4 Internet Protocolu (IP). Bola prvou široko používanou verziou a tvorí základ väčšej časti súčasného Internetu. IPv4 používa 32-bitové adresy, čo obmedzuje adresný priestor jedinečných adries, z ktorých je množstvo vyhradených pre zvláštne účely ako lokálne siete alebo multicastové adresy, čo redukuje počet adries použiteľných ako verejné internetové adresy. Toto obmedzenie pomohlo stimulovať presadzovanie IPv6, ktorý v súčasnosti prechádza skorými štádiami nasadenia a plánuje sa, že postupne celkom nahradí IPv4.

### IPv6
- Hlavným dôvodom vytvorenia IPv6 bol nedostatok adresného priestoru, obzvlášť v husto obývaných krajinách. Predstavenie Network Address Translation (NAT) do určitej miery zmiernilo tento problém. NAT však znemožňuje alebo technicky komplikuje isté peer-to-peer aplikácie ako VoIP. Súčasným prínosom IPv6 sú nové aplikácie ako mobilita, QoS, povinné zabezpečenie atď. IPv6 je druhou verziou IP protokolu formálne prijatou pre široké použitie. Plánom je, aby sa IPv6 stal základom pre budúce rozširovanie internetu.

### Čo je to OSI model
- OSI (Open System Interconnect), je sieťový model, predstavený organizáciou ISO ako štandard, ktorý zjednocuje komunikačné rozhrania, komunikačné jazyky počítačov a sietí a ich prekladače tak, aby sa každé zariadenie pripojené do siete dorozumelo s ľubovoľným ďalším zariadením. V súčasnosti je to primárny model sieťových komunikácii. OSI model sa delí na 7 vrstiev, z ktorých každá opisuje určitú sieťovú funkciu, nevyhnutnú na prenos informácii. Delenie na vrstvy zjednodušuje vývoj čiastkových vlastností a funkcií siete, ako aj zjednodušuje nachádzanie a odstraňovanie problémov. Okrem OSI modelu existujú aj iné sieťové modely, napríklad TCP/IP.
![image](https://github.com/JesusChrist69/maturitne-otazky-SPSIT-KNM-2023/assets/41400711/3726b838-b981-4f28-a182-e9ea16c7e40a)

### Výhody delenia na vrstvy
- OSI model je delený na 7 vrstiev, z ktorých každá predstavuje určitú časť sieťovej komunikácie, Takéto rozdelenie na vrstvy predstavuje rôzne výhody, napríklad:
  - delí prenos informácii do menších, jednoduchších častí
  - poskytuje možnosť vyvíjať jednu vrstvu bez ovplyvnenia inej vrstvy
  - poskytuje kompatibilitu s rôznymi sieťovými štandardmi a zariadeniami
  - delenie na vrstvy je jednoduchšie na vysvetľovanie toku dát v OSI modeli.

**7. Application (Aplikačná)** - táto vrstva je najbližšie k používateľovi, poskytuje sieťové služby užívateľským aplikáciám. Od ostatných vrstiev sa líši tým, že neposkytuje službu žiadnej inej OSI vrstve. Na tejto vrstve pracuje napríklad Browser (Internet Explorer, Netscape Navigator), ktorý používame pri komunikácii cez internet.
**POP3** je spojovo-orientovaný textový protokol ▪ POP3 nie je zabezpečený, jeho šifrovaná podoba sa volá POP3S ▪ Je však autentifikovaný (vyžaduje meno a heslo) ▪ Počúva na porte 110 (šifrovaný na 995) ▪ POP3 dialógy sa volajú transakcie.
**Protokol HTTP** je dnes jedným z najpoužívanejších protokolov, vďaka ktorému existuje služba WWW a služby od nej odvodené ▪ HTTP umožňuje WWW klientovi ▪ Adresovať vzdialený súbor ▪ Požiadať server o jeho zaslanie ▪ Ak sa jedná o skript (napr. PHP), klient žiada, aby mu server poslal výstup behu tohto skriptu, nie skript samotný ▪ Požiadať server o prepísanie tohto súboru.
**IMAP** je klient-server textový protokol ▪ IMAP nie je zabezpečený, jeho šifrovaná podoba sa volá IMAPS ▪ Je však autentifikovaný (vyžaduje meno a heslo) ▪ Počúva na porte 143 (šifrovaný na 993) ▪ Podporuje viacnásobné prihlásenie ▪ Podporuje viac mailboxov (priečinky) na server.
**Protokol DNS** je „telefónny zoznam“ počítačov na internete ▪ My používame slovné názvy počítačov ▪ Počítače používajú číselné IP adresy ▪ DNS slúži na vyhľadanie IP adresy počítača podľa jeho mena ▪ Presnejšie povedané, DNS je stromovo organizovaná databáza, ktorá obsahuje rôzne informácie o internetových menách a adresách.

**6. Presentation (Prezentačná)** - táto vrstva zaisťuje, že údaje odoslané 7.vrstvou posielajúceho počítača sú čitateľné 7.vrstvou prijímacieho počítača. Používa rôzne formátovania, aby zaručila čo najväčšiu kompatibilitu s ostatnými systémami.

**5. Session (Relačná)** - táto vrstva nadväzuje, riadi a ukončuje reláciu medzi dvoma počítačmi, poskytuje svoje služby 6.vrstve OSI modelu. Spravuje prenos dát medzi dvoma systémami a synchronizuje ich komunikáciu

**4. Transport (Transportná)** - zatiaľ čo vrstvy 7, 6 a 5 sa zaoberajú aplikačnými protokolmi, vrstvy 4, 3, 2 a 1 sa zaoberajú prenosom dát v sieti. Transportná vrstva vytvára, spravuje a zatvára virtuálne obvody. Poskytuje spoľahlivý prenos dát, dokáže detektovať chyby v sieti, znovu posielať dáta a dokáže kontrolovať premávku.

**3. Network (Sieťová)** - táto vrstva zabezpečuje spojenie a výber najlepšej cesty spojenia dvoch počítačov v sieti LAN, ale aj WAN, alebo MAN. Je to doména routerov, zaoberá sa logickou sieťovou topológiou.

**2. Data Link (Linková)** - poskytuje spoľahlivé zasielanie dát po médiu. Zaoberá sa fyzickým adresovaním, fyzickou sieťovou topológiou, prístupom k sieti a reguláciou zasielania dát.

**1. Physical (Fyzická)** - táto vrstva definuje elektrické, mechanické a funkčné špecifikácie pre aktiváciu, priebeh a ukončenie fyzického spojenia medzi dvoma systémami. Konkrétne sú tu definované špecifikácie zaoberajúce sa úrovňami napätia, časovaním, maximálnou vzdialenosťou komunikujúcich zariadení, fyzickými spojeniami a ďalšími podrobnými technickými pojmami.

### Porovnanie s TCP/IP
- **TCP/IP (Transmission Control Protocol / Internet Protocol)** - je model používaný v internetovej komunikácii. Tento model umožňuje dvom počítačom umiestneným kdekoľvek, kedykoľvek komunikovať pri zachovaní čo možno najvyššej rýchlosti.
- Podobne ako OSI model, aj **TCP/IP model sa delí na vrstvy**, sú však len 4:
  - **4. Application (Aplikačná)** - táto vrstva je kombináciou vrstiev 7, 6 a 5 z OSI modelu, plní všetky ich funkcie. Všetky operácie týkajúce sa užívateľských aplikácií sa odohrávajú v tejto vrstve.
  - **3. Transport (Transportná)** - plní také funkcie ako Transport vrstva (4) OSI modelu. Obsahuje TCP (Transmission Control Protocol), je to protokol ktorý poskytuje tvorbu vynikajúcich spoľahlivých, rýchlych, a čo najmenej chybových sieťových komunikácii.
  - **2. Internet (Internetová)** - úlohou tejto vrstvy je odoslať požadované data zo siete na vnútornú sieť (internetwork) a zabezpečiť ich doručenie cieľovému počítaču, nezávisle na ceste a sieťach, ktoré bolo potrebné pri tejto úlohe prejsť. Obsahuje IP (Internet Protocol), protokol, ktorý je základom internetu. Na tejto vrstve prebieha zisťovanie najlepšej cesty a tzv. "packet switching"
  - **1. Network Access (Prístupová)** - (aj host-to-network vrstva) táto vrstva obsahuje všetky potrebné procedúry, ktorými musia dáta prejsť, ak majú cestovať po sieti. Obsahuje detaily sietí LAN a WAN a je kombináciou OSI vrstiev 1 a 2. Porovnanie OSI a TCP/IP modelu s prislúchajúcimi si vrstvami uvádzame v tabuľke.
- **Transportná vrstva v TCP/IP**
  - rieši komunikáciu medzi koncovými užívateľmi
  - využíva buď spojovaný a spoľahlivý prenos alebo nespojovaný a nespoľahlivý prenos a nechá to na vyššie vrstvy
  - na transportnej vrstve je TCP protokol – zaisťuje spôľahlivý aj spojovaný prenos, a UDP protokol – zaisťuje nespoľahlivý a nespojovaný prenos
- **Sieťová vrstva v TCP/IP**
  - na nej beží protokol na prepojenie sietí. Naseká na pakety a prepravuje.
  - zaisťuje iba nespoľahlivý a nespojovaný prenos
  - snaží sa byť rýchla
  - zaisťuje prenosové služby nad všetkými vrstvami
  - jediný prenosový protokol v TCP/IP Internet Work
  - výnimky:
    a) SLIP protokol – pripojenie modemom do paketovej siete
    b) PPP protokol- zabezpečuje všetko čo je pod sieťovou vrstvou.

Porovnanie s TCP/IP modelom
![image](https://github.com/JesusChrist69/maturitne-otazky-SPSIT-KNM-2023/assets/41400711/84427c89-79ad-41a1-9ad9-fe1f43d3f518)

#### Definície
- **Prefix** je časť IP adresy, ktorá určuje sieťovú identifikáciu. Napríklad, v IP adrese 192.168.0.1/24 je "24"
- **Maska** (taktiež nazývaná ako maska podsiete alebo sieťová maska) je číslo, ktoré určuje, ktoré bity v IP adrese predstavujú sieťovú a hostovskú časť.

**IP adresy sa tradične delia do dvoch hlavných tried, známych ako triedy IP adries:**
  - **Trieda A**: Adresy triedy A majú prvý bajt IP adresy rezervovaný pre identifikáciu siete, zatiaľ čo zvyšné tri bajty identifikujú konkrétny uzol v sieti. Prvý bajt adresy triedy A je v rozsahu 1 až 126. Tieto adresy majú veľmi veľký rozsah sietí a môžu obsahovať veľký počet uzlov. Príkladom adresy triedy A je 10.0.0.1.
  - **Trieda B**: Adresy triedy B majú prvá dva bajty vyhradené pre identifikáciu siete, zatiaľ čo posledné dva bajty identifikujú konkrétny uzol v sieti. Prvé dva bajty adresy triedy B sú v rozsahu 128 až 191. Tieto adresy sú vhodné pre stredne veľké siete. Príkladom adresy triedy B je 172.16.0.1.

- **Sieťová adresa**: Sieťová adresa je adresa, ktorá identifikuje konkrétnu sieť. V rámci počítačových sietí je sieťová adresa časť IP adresy, ktorá určuje, do akej siete patrí určitý uzol alebo zariadenie. Sieťová adresa je spoločná pre všetky zariadenia v danej sieti. Pomocou sieťovej adresy sa vykonáva smerovanie paketov v sieti, aby sa dosiahol správny uzol.

- **Všeobecná adresa**: Všeobecná adresa (tiež nazývaná rozširovacia adresa alebo broadcastová adresa) je špeciálna adresa, ktorá je určená pre všetky uzly v danej sieti. Keď zariadenie odosiela paket na všeobecnú adresu, je to interpretované ako žiadosť o poslanie paketu na všetky zariadenia v rámci danej siete. Týmto spôsobom môže zariadenie komunikovať so všetkými uzlami v sieti naraz.

- **Maska podsiete** (tiež nazývaná podsieťová maska alebo sieťová maska) je číselná hodnota používaná v IP adresácii na identifikáciu siete a uzlov v rámci siete. Táto maska určuje, ktoré bity v IP adrese predstavujú sieťovú časť a ktoré bity predstavujú časť uzla. Maska podsiete sa zapisuje ako číslo, ktoré udáva počet po sebe idúcich bitov s hodnotou 1 v binárnej reprezentácii. Je to obvykle 32-bitová hodnota v prípade IPv4 adries a 128-bitová hodnota v prípade IPv6 adries. V maskách podsiete sú bity s hodnotou 1 označené ako sieťová časť, zatiaľ čo bity s hodnotou 0 predstavujú časť uzla.

- **Podsieť** je časť siete, ktorá vznikne rozdelením pôvodnej siete na menšie podsiete. Rozdelenie siete na podsiete sa často používa na zlepšenie efektivity správy siete a umožňuje lepšie riadenie a organizáciu sieťových zariadení a pripojených uzlov. Každá podsieť má svoju vlastnú unikátnu sieťovú adresu a rozsah IP adries pridelených tejto podsieti. Tieto IP adresy sa používajú na identifikáciu uzlov v rámci danej podsiete. Každá podsieť má tiež svoju vlastnú masku podsiete, ktorá určuje, ktoré bity IP adresy patrí do sieťovej časti a ktoré bity sú určené pre uzly.


[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
