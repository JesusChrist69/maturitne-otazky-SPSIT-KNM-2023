# 11. Charakteristika arduina
piny arduina, ich použitie, využitie arduina pre riadenie, vývojové prostredie pre tvorbu zdrojového kódu Arduino, základná štruktúra programu pre arduino, premenné, ich platnosť a základné programové štruktúry, vplyv mikrokontrolérov na rozvoj internetu vecí, digitálny a analógový signál

### Využitie arduina pre riadenie
- uzatvorený regulačný obvod – napr. regulácia teploty, vlhkosti...

### Vývojové prostredie pre tvorbu zdrojového kódu Arduino
-	je viacplatformová aplikácia, naprogramovaná v Jave. Je navrhnuté tak, aby umožnilo programovať aj ľuďom, ktorí nemajú veľké skúsenosti s programovaním. Obsahuje editor kódu s bežnými vlastnosťami ako farebné označovanie syntaxe, automatické zarovnávanie a párovanie zátvoriek. Je schopné program skompilovať a nahrať do Arduina jedným kliknutím tlačidla. Program pre Arduino sa pomenúva anglickým slovom sketch
-	Programovací jazyk pre Arduino vychádza z jazyka C/C++. Je to vlastne céčko obohatené o knižnice pre Arduino. Arduino IDE obsahuje knižnice pre prácu so sériovým portom, LCD displejmi, SPI, WiFi, SD kartami, krokovými a servo motormi a veľa ďalšími.
-	Arduino IDE je program, pomocou ktorého píšete programy pre Arduino. Keď máte program hotový, odošlete ho do Arduina, kde sa spustí. IDE umožňuje spravovať aktuálne verzie dosiek a nainštalovaných knižníc.
- ![image](https://github.com/JesusChrist69/maturitne-otazky-SPSIT-KNM-2023/assets/41400711/36dc48af-8f11-4867-be0f-608ad4882099)
- Na obrázku sú popísané jednotlivé tlačítka (zľava doprava) kontrola a kompilovanie (Verify), nahranie (Upload), Nová skica (New), Otvoriť (Open) a Uložiť (Save).

### Základná štruktúra programu pre arduino
-	Vo vývojovom prostredí sa na programovanie dosiek Arduino používa jazyk C/C++.
-	Program pozostáva z dvoch častí - z procedúry pre nastavenie void setup() a z výkonného cyklu void loop(). V nastavení sa definujú konštanty, premenné a inštancie objektov.
-	Následne sa tam vykoná aj inicializácia všetkých použitých objektov. V tele výkonného cyklu sa nachádza postupnosť inštrukcií, ktorá sa začne opakovane vykonávať po ukončení nastavovacej procedúry.
-	Program musí vždy obsahovať obe časti, v opačnom prípade skončí chybou

### Premenné, ich platnosť a základné programové štruktúry
-	Premenné sú pamäťové miesta prístupné prostredníctvom identifikátoru. Hodnotu premenných môžeme počas výpočtu meniť. Tým sa premenné zásadne odlišujú od konštánt, ktoré majú po celú dobu chodu programu hodnotu nemennú 
-	Premenné deklarujeme uvedením dátového typu

```if```
- Ak chceme, aby sa určitá časť kódu vykonala len v určitých prípadoch, prichádzajú na rad podmienky

```if… else```
- Operácia “if… else” umožňuje rozhodovanie štýlom “buď – alebo” a vetvenie programu podľa výsledku operácie

```switch case```
- Switch je špeciálny druh podmienky. Špeciálny je v tom, že sa zaoberá iba premennou a jej hodnotou. Program prechádza každú vetvu konštrukcie switch a testuje hodnotu premennej. Ďalší rozdiel je v tom, že sa môže vykonať aj viac vetiev (čo u if sa nedá)

```for```
- Cyklus je časť programu, ktorý je v závislosti na podmienke vykonávaný opakovane. U cyklu obvykle rozlišujeme riadiacu podmienku cyklu a telo cyklu.

```while```
- Všetky príkazy v cykle sa vykonávajú, pokiaľ je podmienka pravdivá. Za zmienku stojí, že program kontroluje platnosť podmienky vždy na začiatku cyklu, ak je nepravdivá, cyklus skončí. 

```do… while```
- Cykly while a do…while sú si veľmi podobné a líšia sa len prvým priebehom. U while sa podmienkový výraz vyhodnotí pred prvým prevedením tela cyklu, zatiaľ čo u do…while sa telo prevedie vždy aspoň raz.

```break a continue```
- V jazyku C existujú ešte dve riadiace štruktúry, ktoré ovplyvňujú vykonávanie cyklov. Je to break a continue. Príkaz break ukončí okamžite vykonávanie cyklu a program nasleduje prvým príkazom za cyklom, continue okamžite ukončí aktuálnu iteráciu a začne novú. 


### Vplyv mikrokontrolérov na rozvoj internetu vecí
– jednočípový mikropočítač, je schopný samostatnej funkcie. Okrem procesora obsahuje aj pamäť, programovateľné I/O rozhrania a ďalšie periférne obvody (čítač, časovač, porty...). Sú takmer v každom modernom elektronickom prístroji: riadenie auta, lekárske prístroje, implantáty, diaľkové ovládače, hračky
-	digitálny signálový procesor (DSP), zameraný na spracovanie signálov. Je optimalizovaný na čo najrýchlejšie opakovanie jednoduchých matematických algoritmov. Využitie v satelitných telekomunikačných sieťach, zosilňovačoch..

### Digitálny a analógový signál
-	**Digitálne** - môže byť vo všeobecnosti iba jedna z dvoch hodnôt 0 alebo 1, ide o binárnu hodnotu (neplatí pre PWM výstup).
  - **Hodnota 0** znamená, že na digitálnom pine je elektrické napätie 0V, teda GND (alebo menej ako 2V pre vstup). Túto skutočnosť môžeme vyjadriť stavmi LOW alebo 0.
  - **Hodnota 1** znamená, že na digitálnom pine je elektrické napätie +5V (alebo viac ako 3V pre vstup). Túto skutočnosť môžeme vyjadriť stavmi HIGH alebo 1.
  - Pri digitálnych výstupných pinoch v móde PWM sa na pin posiela celé číslo z rozsahu 0 až 255. Veľmi zjednosušene si to môžeme predstaviť ako namapovaný rozsah el. napätia 0V až 5V do číselného intervalu 0 až 255 a zariadenie pripojené na takýto výstup sa chová, akoby sme zmenou číselnej hodnoty 0-255 na pine zmenili el. napätie na zariadení. Praktické využitie je napr. pri postupnom rozsvecovaní a zhasínaní LED
  - Digitálny **pin č.13** (LED_BUILTIN) je už priamo spojený s LED na doske

- **Analógové** - Pri použití analógových vstupných pinov tieto pracujú ako A/D prevodník a nadobúdajú hodnoty od 0 do 1023 v závislosti od elektrického napätia na vstupnom analógovom pine. Tento rozsah 0V-5V možno zmeniť buď softvérovo alebo privedením referenčného el. napätia 


[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
