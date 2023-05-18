# 7. Ethernet a prepínače
činnosť Ethernetu, fungovanie prístupovej metódy Ethernetu (CSMA/CD,CA), MAC adresa, Ethernetový rámec a jeho polia, typy ethernetových portov na prepínači, konfigurácia ethernetových portov v Cisco IOS, typy prepínačov, princíp prepínania, ďalšie sieťové zariadenia, kolízne a vysielacie (broadcastové) domény, VLAN, dôvody ich konfigurácie, spôsob konfigurácie VLAN, funkcia trunk_u, spôsob komunikácie medzi rôznymi VLAN

- **Ethernet** je založený na nápade, že počítače v sieti budú posielať správy spôsobom, ktorý pripomína rádio, ale prostredníctvom spoločného kábla alebo kanála, niekedy označovaného ako éter (ether). Každý počítač má globálne jedinečnú 48-bitovú MAC adresu, ktorú má každá karta pridelenú od výroby, aby bolo zabezpečené, že všetky systémy v spoločnom Ethernete majú rozdielne adresy. Vďaka dnešnej všadeprítomnosti Ethernetu zabudovali mnohí výrobcovia ethernetové karty priamo do matičných dosiek počítačov.

### I. CSMA/CD
- Collision Detection, detekcia kolízií. Rieši postup uzla, ak je médium obsadené. CSMA/CD má dva varianty:
  - **Nenaliehajúca metóda** CSMA/CD (non-persistent CSMA/CD). Ak je kanál obsadený, uzol počká na náhodne zvolený časový okamih a znovu testuje stav kanálu. To sa opakuje, pokiaľ sa vysielanie neuskutoční. Náhodne dlhé čakanie minimalizuje pravdepodobnosť, že dva uzly čakajúce na uvoľnenie média začnú vysielať naraz po jeho uvoľnení.
  - **Naliehajúca metóda** (persistent CSMA/CD). Ak je kanál obsadený, stanica odloží vysielanie na okamih jeho uvoľnenia (podobne ako nedočkaví slušní ľudia). Nevýhodou tejto jednoduchej metódy, je riziko kolízie s uzlami, ktoré tiež čakajú na uvoľnenie kanálu. 

### II. CSMA/CA
- Collision Avoidance, predchádzanie kolíziám. Ak je kanál voľný, vysielač musí najprv informovať ostatné uzly o úmysle vysielať, až verzia 20210317.2249 následne môže vysielať, predchádza kolíziám. Často sa využíva v bezdrôtových sieťach, kde nie je možné súčasne vysielať aj prijímať.

### Definície
- **MAC adresa** je jednoznačný identifikátor sieťového zariadenia, ktorý používajú rôzne protokoly druhej vrstvy OSI. Je priraďovaná sieťovej karte bezprostredne pri jej výrobe, a preto sa jej tiež niekedy hovorí fyzická adresa, avšak je ju možné u moderných kariet dodatočne zmeniť

- **Ethernetový rámec** je v informatike protokolová dátová jednotka linkovej vrstvy v sieti Ethernet. Na fyzickej vrstve mu predchádza preambula a oddeľovač začiatku rámca , ktoré s ethernetovým rámcom tvoria paket. Ethernetový rámec začína ethernetovou hlavičkou, ktorá obsahuje cieľovú a zdrojovú MAC adresu  a pole Dĺžka/Typ . Ďalej obsahuje dátové pole  a kontrolnú postupnosť rámca, čo je 32-bitový cyklický redundantný súčet používaný na detekciu poškodenia dát pri prenose. Dátové pole začína v ethernetovom rámci hlavičkou protokolu

- **LAN port RJ-45** – nejběžnější port pro připojení počítačů, notebooků, síťových tiskáren a dalších periferií. SFP – speciální konektor využívající optická vlákna, propustnost až 1000 Mbit/s. Dual Personality – dvojité konektory, které obsahují jak RJ-45, tak port SFP.

### Sieťové zariadenia
- **Repeater** – opakovač – obnovuje signál, ktorý na fyzicky dlhšom úseku siete degraduje, stráca pôvodné charakteristiky (silu a tvar)
- **Hub** – rozbočovač – spája niekoľko segmentov siete do segmentu jedného (prevádzka v jednej časti siete sa prenesie aj do častí ďalších sietí)
- **Bridge** – most – spája dva fyzicky oddelené segmenty siete
- **Switch** – prepínač – spája dve a viac zariadení v rámci jedného alebo viacerých segmentov siete, oddeľuje sieťovú prevádzka (nezaťažuje ostatné časti siete)
- **Router** – smerovač – presmerováva komunikáciu do iného segmentu rovnakého typu siete
- **Gateway** – brána – sprostredkováva komunikáciu dvoch odlišných typov siete

### Domény
- **Broadcastová doména** je v informatike časť počítačovej siete, v ktorej môže na linkovej vrstve ISO/OSI modelu každý sieťový uzol komunikovať s každým pomocou broadcastu. Broadcastovú doménu tvorí jeden segment siete alebo vo viacerých segmentoch pomocou mosta. Broadcastovú doménu rozdeľuje router alebo gateway.
- Zvyšovaním počtu stanic v segmente narastá pravdepodobnosť kolizie a výsledkom je viac opakovaných prenosov. Riešením je rozdeliť **kolíznu doménu** na niekoľko menších, oddelených častí. Pri prepájaní využívajú bridže tabuľku MAC adres asociovanú s portami

### VLAN
- **VLAN** je výraz pre jednu logickú sieť  po zavedení tohto modelu **LAN**. Zmysel koncepcie VLAN je možné vhodne načrtnúť ako zefektívnenie využitia aktívnych intermediárnych prvkov siete ale tiež jej prvkov pasívnych, popr. uľahčenie správy siete kedy v prostredí s prekladaným výskytom užívateľov rôzneho druhu je možné agregovať koncové zariadenia na jednu fyzickú infraštruktúru

- **Statické VLAN** sú porty na prepínači, ktoré sú manuálne pridelené do VLAN použitím VLAN manažment aplikácie alebo pracujú priamo vnútri prepínača. Statické siete dobre pracujú v sieťach kde:
  - presuny sú kontrolované a manažované
  - kde je veľký VLAN manažment softvér na konfigurovanie portov

- **TRUNK** je taký prepoj, kde sa mixujú rámce s rôznych VLAN. Teda pokiaľ v jednom sieťovom prepoji môže prúdiť viacero sieťových správ z rôznych VLAN, hovoríme že takýto prepoj je TRUNK.
  - Prepínač filtruje dopravu, komunikácia je v rámci segmentu, pri požiadavke o komunikáciu mimo segmentu je rámec presunutý na správne rozhranie.

[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
