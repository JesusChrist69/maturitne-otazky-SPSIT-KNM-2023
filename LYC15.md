# 15. Pamäťový systém
parametre pamäte, rozdelenie pamätí, hierarchické usporiadanie, operačná pamäť, výmena údajov medzi hlavnou a vyrovnávacou pamäťou, algoritmy vyradzovania blokov z pamäte, pseudonáhodný výber, pamäťové moduly SRAM, DRAM, SD RAM, typy pamäťových modulov, vonkajšie pamäte

### Parametre pamäte
-	kapacita vyjadrená je celkovým počtom bytov alebo slov, ktoré môžu byť. súčasne uložené v pamäti
-	prístupová doba - je čas, za ktorý sú dáta načítané alebo uložené
- prenosová rýchlosť - počet údajov prenesených z/do pamäte ako súvislý blok za jednotku času (MB/s).
-	Poruchovosť - stredná doba medzi dvoma poruchovými stavmi – udáva sa v hodinách.
-	spotreba - elektrický príkon pripadajúci na jeden bit. (nW/b, μW/b).
-	rozdeľte pamäte podľa energetickej závislosti, materiálu, na ktorom sú dáta uložené, práce 
  -	Energeticky nezávislá (Non-volatile) nemiznúce – pamäť, ktoré si zachováva svoj obsah aj po vypnutí napájania
  -	Energeticky závislá (Volatile) – pamäť, ktorá po vypnutí napájania stratí svoj obsah
-	s informáciou (len čítanie, viacnásobné čítanie a zápis jeden krát, viacnásobný zápis)
  - umožňujúca len čítanie informácií (ROM, CD, DVD, BluRay...)
  - umožňujúca jeden zápis a viacnásobné čítanie (CD-R, DVD-R...)
  - umožňujúca opakovaný zápis aj čítanie (EPROM, HDD, CD-RW, Flash...)

### Operačná pamäť
-	Hlavná (operačná, RAM) pamäť slúži na ukladanie dát bežiacich programov a operačného systému počítača. Ako už z názvu vyplýva, je to pamäť s náhodným, resp. ľubovoľným prístupom. Musí byť rýchla, musí mať možnosť čítať a zapisovať dáta. Dnes sú výhradne polovodičové. Sú veľmi rýchle, čas zápisu do pamäte je rovnaký bez ohľadu na umiestnenie údaja v pamäti.
- je realizovaná ako samostatný funkčný blok, ktorý sa skladá z jedného alebo niekoľkých integrovaných obvodov.
- hlavná pamäť je vo väčšine osobných počítačov realizovaná dynamickými pamäťami, ktoré majú pri nízkej spotrebe energie veľkú kapacitu.

### Výmenu údajov medzi hlavnou a vyrovnávacou pamäťou
- vyrovnávacia pamäť obsahuje kópie len malého množstva pamäťových miest z hlavnej pamäte, preto je nutné stanoviť optimálnu metódu ich výberu.
- ak sa vyrovnávacia pamäť zaplní, musíme voliť, ktoré bloky vyradíme
- kvôli efektivite sa nepracuje s bajtmi údajov, ale s celými blokmi (niekoľko bajtov)

### Algoritmy vyradzovania blokov z pamäte
-  **LRU** (Least Recently Used) – vyradí sa blok, ktorý je najmenej používaný
  - najzložitejšia realizácia
  - každý blok má čítač
    - ak pristupujeme ku bloku, tak sa jeho čítač vynuluje a čítačom ostatných blokov sa pripočíta jednotka
  - vyradí sa blok, ktorý má hodnotu čítača najvyššiu
   
- **FIFO** (First In, First Out- fronta) – vyradí sa blok, ktorý je v cache najdlhšie
  - jednoduchšie
  - každý blok má opäť čítač, ktorý sa zväčší o jednotku pri každom prístupe do cache
  - vyradí sa blok s najväčším číslom

- **LIFO** - Last-In-First-Out – zásobník
  - vyradí sa blok, ktorý prišiel posledný
  - pseudonáhodný výber
  - najjednoduchší
  - vyššie uvedené algoritmy znižujú SVB pomerne málo, preto sa niekedy používa iba náhodný výber

### Vonkajšie pamäte
- Pevný disk (HDD), SSD, USB, CD, DVD...

[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
