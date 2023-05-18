# 14. Základné dosky, zbernice a rozhrania
základná doska, štandardizácia dosiek, rôzne formáty dosiek, časti základnej dosky, BIOS, príklady použitia, BIOS vo vrstvovom modeli počítača, typy čipov, základne funkcie BIOSu, spôsob bootovania PC, pípacie kódy, funkcia pamäte CMOS, čipová sada, základné typy I/O zberníc, rozdelenie zberníc, rôzne typy rozhraní

### Základná doska
- Základná doska je hlavnou súčasťou počítača, ktorá poskytuje pripojenie a komunikáciu medzi všetkými hardvérovými komponentmi.
- Obsahuje rôzne konektory, sloty a čipové sady na pripojenie procesora, pamätí, rozširujúcich kariet, úložných zariadení, zvukovej karty, sieťovej karty a ďalších komponentov.
- Na základnej doske sa nachádza tiež BIOS (Basic Input/Output System), ktorý zabezpečuje správne načítanie systému a komunikáciu s periférnymi zariadeniami.

### Štandardizácia dosiek
- Existujú rôzne štandardy pre základné dosky, ktoré definujú fyzické rozloženie konektorov a špecifikácie komunikačných rozhraní.
- Napríklad pre PC sú najbežnejšie štandardy ATX (Advanced Technology Extended), Micro-ATX a Mini-ITX.

### Rôzne formáty dosiek
- **ATX**: Najbežnejší formát pre desktopové počítače.
- **Micro-ATX**: Menšia verzia ATX s obmedzeným počtom rozširujúcich slotov.
- **Mini-ITX**: Malý formát využívaný pre kompaktné a energeticky efektívne počítače.

### Časti základnej dosky
- Procesorový soket: Slúži na pripojenie procesora.
- Pamäťové sloty: Slúžia na pripojenie pamäťových modulov (RAM).
- Rozširujúce sloty: Umožňujú pripojenie rozširujúcich kariet (napr. grafická karta, sieťová karta).
- Čipová sada (Chipset): Riadi komunikáciu medzi rôznymi časťami základnej dosky.
- Periférne konektory: Zabezpečujú pripojenie rôznych periférnych zariadení (napr. USB, zvukové konektory, Ethernet).
- BIOS (Basic Input/Output System): Firmware zodpovedný za inicializáciu a konfiguráciu hardvéru počítača.

### BIOS
- BIOS je skratka pre Basic Input/Output System.
- Nachádza sa na základnej doske a slúži na inicializáciu a konfiguráciu hardvéru počítača pri štarte.
- Poskytuje základné rozhranie pre komunikáciu medzi operačným systémom a hardvérom.
- Umožňuje nastavenie parametrov systému, ako sú dátum a čas, bootovacie zariadenie, správa napájania a ďalšie.

### Príklady použitia BIOSu
- Nastavenie bootovacieho poradia (výber, ktoré zariadenie sa načíta ako prvé pri štarte).
- Nastavenie parametrov systému, ako je dátum, čas a správa napájania.
- Aktualizácia firmware základnej dosky (v niektorých prípadoch).

### BIOS vo vstvovom modeli počítača
- Vrstvový model počítača je abstraktný model, ktorý rozdeľuje softvér a hardvér do niekoľkých vrstiev.
- BIOS sa nachádza v najnižšej vrstve modelu, známej ako "Firmware layer" (vrstva firmware).
- Firmware layer je zodpovedný za inicializáciu hardvéru a poskytuje základné rozhranie pre vyššie vrstvy.

### Typy čipov
- Základná doska obsahuje rôzne čipy, ktoré vykonávajú rôzne úlohy.
- Čipová sada (Chipset): Riadi komunikáciu medzi procesorom, pamäťou, periférnymi zariadeniami a ďalšími časťami základnej dosky.
- Čip BIOSu: Obsahuje firmvér BIOS, ktorý je zodpovedný za správnu inicializáciu systému a komunikáciu s periférnymi zariadeniami.

### Základné funkcie BIOSu
- Power-On Self-Test (POST): Testuje hardvér počítača po zapnutí.
- Načítanie a spustenie operačného systému zo zvoleného zariadenia (bootovanie).
- Konfigurácia hardvéru a základných parametrov systému.
- Poskytovanie rozhrania pre aktualizáciu firmware základnej dosky.
- Riadenie správy napájania a spotreby energie.

### Spôsob Bootovania PC
- Po zapnutí počítača BIOS vykoná POST (Power-On Self-Test), testuje hardvér a identifikuje prítomné zariadenia.
- BIOS potom vyhľadá a načíta bootovací sektor z vybraného zariadenia (napr. pevný disk, USB kľúč) podľa nastaveného bootovacieho poradia.
- Bootovacý sektor obsahuje malý program, ktorý začne načítavať operačný systém a preda kontrolu ďalším častiam počítača.

### Pípacie kódy
- Pípacie kódy (beep kódy) sú zvukové signály produkované BIOSom počítača.
- Slúžia na indikáciu rôznych problémov alebo chýb počas POST (Power-On Self-Test).
- Každý výrobca môže mať vlastné pípacie kódy, ktoré poskytujú špecifické informácie o chybách.

### Funkcia pamäte CMOS
- CMOS (Complementary Metal-Oxide-Semiconductor) je typ pamäte používanej v BIOS čipe.
- CMOS pamäť uchováva nastavenia systému (napríklad dátum, čas, konfigurácia) aj po vypnutí počítača a odpojení od napájania.
- Pamäť CMOS je malá a spotrebuje veľmi málo energie, čo umožňuje uchovávať nastavenia aj pri absencii napájania.

### Čipová sada (Chipset)
- Čipová sada je sada integrovaných čipov na základnej doske, ktoré riadia a koordinujú komunikáciu medzi rôznymi časťami počítača.
- Čipová sada zahŕňa rôzne podčipy, ako sú Northbridge a Southbridge (v starších systémoch) alebo jednotný čip (v moderných systémoch).
- Northbridge sa zaoberá komunikáciou medzi procesorom, pamäťou a grafickou kartou.
- Southbridge zabezpečuje komunikáciu s periférnymi zariadeniami, ako sú pevné disky, USB, zvukové karty atď.

### Základné typy I/O zberníc
- **ISA** (Industry Standard Architecture): Starší štandard, ktorý poskytoval rozhranie pre rozširujúce karty.
- **PCI** (Peripheral Component Interconnect): Predchodca PCI Express, poskytuje vysokorýchlostné rozhranie pre rôzne rozširujúce karty.
- **AGP** (Accelerated Graphics Port): Špeciálne rozhranie pre pripojenie grafickej karty, ktorý poskytoval vysokú priepustnosť dát pre lepšiu grafiku.
- **PCI Express**: Moderné vysokorýchlostné sériové rozhranie pre pripojenie rôznych rozširujúcich kariet (napr. grafická karta, sieťová karta).

### Rozdelenie zberníc
- **Von Neumannova architektúra**: Základný model počítača, kde dáta a programy sa nachádzajú v jednej pamäti a zdieľajú spoločnú zbernicu.
- **Harvardova architektúra**: Model, ktorý oddeluje dáta a programy do samostatných pamätí a zberníc, čo umožňuje paralelnú prácu s dátami a programami.

### Rôzne typy rozhraní
- **USB** (Universal Serial Bus): Univerzálne rozhranie pre pripojenie rôznych periférnych zariadení, ako sú klávesnice, myši, tlačiarne atď.
- **Ethernet**: Rozhranie pre pripojenie k počítačovej sieti, umožňuje komunikáciu medzi počítačmi a zdieľanie sietových zdrojov.
- **HDMI** (High-Definition Multimedia Interface): Rozhranie pre prenos audio a video signálov vo vysokom rozlíšení medzi počítačom a zobrazovacím zariadením.
- **SATA** (Serial ATA): Rozhranie pre pripojenie úložných zariadení, ako sú pevné disky a SSD, umožňuje rýchlu prenosovú rýchlosť dát.
- **PCIe** (Peripheral Component Interconnect Express): Vysokorýchlostné sériové rozhranie pre pripojenie rozširujúcich kariet, ako sú grafické karty, sieťové karty a ďalšie.

[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
