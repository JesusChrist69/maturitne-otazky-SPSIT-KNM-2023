# 10. Rastrová a vektorová grafika
rastrová a vektorová grafika, druhy grafických formátov, vlastnosti, vlastnosti modelu RGB a CMYK, práca s rastrovým grafickým editorom, práca s vektorovým grafickým editorom

- Rastrová a vektorová grafika sú dva rôzne typy formátov digitálnych obrázkov používaných v počítačovej grafike.

- **Rastrová grafika**, známa aj ako bitmapová grafika, je tvorená mriežkou jednotlivých pixelov, kde každý pixel obsahuje informácie o farbe. Tieto obrázky sú závislé od rozlíšenia, čo znamená, že sa skladajú zo špecifického počtu pixelov a majú pevnú veľkosť. Bežné formáty rastrových súborov zahŕňajú JPEG, PNG, GIF a BMP. Rastrová grafika je najvhodnejšia na znázornenie obrázkov so súvislými tónmi, ako sú fotografie a zložité ilustrácie, kde sú dôležité jemné detaily a farebné variácie.
  - Hlavnou výhodou rastrovej grafiky je jej schopnosť zobrazovať vysoko detailné a realistické obrázky. Majú však obmedzenia, pokiaľ ide o zmenu mierky a úpravy. Zväčšenie rastrového obrázku nad jeho pôvodnú veľkosť môže mať za následok stratu kvality a pixelácie, pretože jednotlivé pixely budú viditeľnejšie. Navyše, keďže každý pixel obsahuje informácie o farbe, úprava konkrétnych prvkov alebo tvarov v rastrovom obrázku môže byť náročná.

- Na druhej strane **vektorová grafika** pozostáva z matematických vzorcov, ktoré definujú čiary, krivky a tvary. Namiesto použitia pixelov vektorová grafika ukladá informácie o vzťahoch medzi týmito geometrickými prvkami. Výsledkom je, že vektorová grafika je nezávislá od rozlíšenia, čo znamená, že ju možno zväčšiť alebo zmenšiť bez straty kvality. Bežné formáty vektorových súborov zahŕňajú SVG (Scalable Vector Graphics), AI (Adobe Illustrator) a EPS (Encapsulated PostScript).

### Využitie
- Stručne povedané, rastrová grafika je najlepšia na znázornenie obrázkov so súvislými tónmi a ponúka vysoké detaily, zatiaľ čo vektorová grafika je vhodná pre geometrické ilustrácie, logá a škálovateľnú grafiku. Voľba medzi rastrovou a vektorovou grafikou závisí od konkrétnych požiadaviek projektu a zamýšľaného použitia obrázkov.

### Druhy grafických formátov, vlastnosti

- **JPEG (Joint Photographic Experts Group)**: JPEG je široko používaný formát stratovej kompresie pre rastrové obrázky. Je vhodný pre fotografie a zložité obrázky s plynulými prechodmi farieb. Súbory JPEG možno komprimovať, aby sa zmenšila veľkosť súboru, ale môže dôjsť k určitej strate kvality obrazu.

- **PNG (Portable Network Graphics)**: PNG je bezstratový kompresný formát pre rastrové obrázky. Podporuje priehľadnosť a bežne sa používa pre webovú grafiku a obrázky, ktoré vyžadujú priehľadné pozadie. Na rozdiel od JPEG súbory PNG nestratia kvalitu obrazu pri kompresii.

- **GIF (Graphics Interchange Format)**: GIF je formát bežne používaný pre animované obrázky. Podporuje animácie a umožňuje kombinovať viacero snímok do jedného súboru. GIF tiež podporuje priehľadnosť, vďaka čomu je užitočný pre jednoduchú grafiku a logá.

- **BMP (Bitmap)**: BMP je nekomprimovaný rastrový formát, ktorý ukladá informácie o farbe každého pixelu jednotlivo. Bežne sa používa v aplikáciách založených na systéme Windows, ale používa sa menej často kvôli väčším veľkostiam súborov v porovnaní s komprimovanými formátmi.

### Vlastnosti modelu RGB a CMYK
- RGB a CMYK sú farebné modely používané na reprezentáciu a reprodukciu farieb v rôznych kontextoch. Tu sú ich hlavné vlastnosti:

- **RGB** (červená, zelená, modrá):
  - **Aditívny farebný model**: RGB je aditívny farebný model, čo znamená, že farby sa vytvárajú spojením rôznych intenzít červeného, zeleného a modrého svetla. Keď sa všetky tri farby skombinujú v plnej intenzite, vytvoria biele svetlo.
  - **Farebný rozsah**: RGB má široký farebný rozsah a môže reprezentovať široký rozsah živých a nasýtených farieb. Je vhodný na zobrazenie živých digitálnych obrázkov a grafiky.

- **CMYK** (azúrová, purpurová, žltá, kľúčová/čierna):
  - **Subtraktívny farebný model**: CMYK je subtraktívny farebný model, čo znamená, že farby sa vytvárajú odčítaním rôznych množstiev azúrového, purpurového, žltého a čierneho atramentu od bieleho pozadia. Keď sa všetky štyri atramenty skombinujú pri plnej intenzite, pohltia všetko svetlo a vytvoria čiernu farbu.
  - **Tlač a reprodukcia**: CMYK sa primárne používa v tlačových procesoch vrátane ofsetovej tlače, digitálnej tlače a komerčnej tlače. Pri týchto procesoch sa farby reprodukujú prekrytím poltónových bodov azúrového, purpurového, žltého a čierneho atramentu.

### Editor rastrovej grafiky
- **Pixel-based**: Rastrové grafické editory pracujú s obrázkami, ktoré sa skladajú z jednotlivých pixelov. Každý pixel obsahuje informácie o farbe a obrázok je v podstate mriežkou týchto pixelov. Úprava zahŕňa úpravu a manipuláciu s jednotlivými pixelmi alebo skupinami pixelov.

- **Závisí od rozlíšenia**: Rastrové obrázky majú pevné rozlíšenie určené počtom pixelov. Zväčšenie rastrového obrázka nad jeho pôvodnú veľkosť môže viesť k strate kvality a pixelizácii. Úpravy zahŕňajú prácu s určitým počtom pixelov a vykonané zmeny ovplyvňujú priamo pixely.

- **Najlepšie pre obrázky so súvislými tónmi**: Editory rastrovej grafiky vynikajú v práci s obrázkami so súvislými tónmi, ako sú fotografie, zložité ilustrácie a podrobné digitálne umelecké diela. Dokážu presne zachytiť jemné detaily, textúry a farebné variácie.

- **Nástroje na úpravu**: Editory rastrovej grafiky poskytujú nástroje na prácu s jednotlivými pixelmi a úpravu obrázka na detailnej úrovni. Tieto nástroje zahŕňajú štetce, gumy, nástroje na výber, filtre a úpravy na manipuláciu s farbami, tónmi a efektmi.

### Editor vektorovej grafiky
- **Objektové**: Editory vektorovej grafiky pracujú s matematickými vzorcami, ktoré definujú čiary, krivky a tvary. Obrázky sú konštruované z týchto geometrických prvkov, známych ako vektory. Úprava zahŕňa manipuláciu a úpravu vlastností týchto vektorov.

- **Nezávislé na rozlíšení**: Vektorové obrázky sú nezávislé na rozlíšení, čo znamená, že ich možno zväčšiť alebo zmenšiť bez straty kvality. Keďže sú založené na matematických vzorcoch, zmeny vykonané na vektorovom obrázku nemajú vplyv na ostrosť alebo jasnosť obrázka.

- **Najlepšie pre geometrické ilustrácie**: Editory vektorovej grafiky sú ideálne na vytváranie log, ikon, typografie, technických ilustrácií a akejkoľvek grafiky, ktorá vyžaduje presné tvary, hladké línie a škálovateľnosť. Nie sú vhodné na zobrazenie zložitých textúr a obrázkov so súvislými tónmi.

- **Nástroje na úpravu**: Editory vektorovej grafiky poskytujú nástroje na vytváranie a úpravu vektorových objektov. Tieto nástroje zahŕňajú nástroje na kreslenie, nástroje na tvarovanie, nástroje pera na vytváranie kriviek, nástroje na výber a transformačné nástroje na zmenu veľkosti, otáčanie a skosenie objektov. Ponúkajú tiež možnosti použitia výplní, ťahov a prechodov na objekty.


[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
