# 17. Programovací jazyk - vetvenie
druhy vetvení, všeobecné tvary (syntax), vlastnosti a rozdiely medzi nimi, porovnanie metódy vetvenia v C++ s metódami v inom programovacom jazyku napr. Java, C#, PHP, JavaScript, Pascal, atď.

### Druhy vetvení
- Vetvenie "**if**": Vykoná kód, ak je podmienka splnená.
- Vetvenie "**if-else**": Vykoná kód v bloku "if", ak je podmienka splnená, inak vykoná kód v bloku "else".
- Vetvenie "**if-else if-else**": Umožňuje vyhodnotiť viacero podmienok za sebou a vykonať príslušný kód pre prvú splnenú podmienku.
- Vetvenie "**switch**": Porovnáva hodnotu premennej s rôznymi možnými hodnotami a vykoná príslušný kód pre zhodujúcu sa hodnotu.

### Syntax
- Vetvenie **if**
```
if (podmienka) {
  // kód na vykonanie, ak je podmienka splnená
}
```

- Vetvenie **if-else**
```
if (podmienka) {
  // kód na vykonanie, ak je podmienka splnená
} else {
  // kód na vykonanie, ak podmienka nie je splnená
}
```

- Vetvenie **if-else if-else**
```
if (podmienka1) {
  // kód na vykonanie, ak je podmienka1 splnená
} else if (podmienka2) {
  // kód na vykonanie, ak podmienka1 nie je splnená a podmienka2 je splnená
} else {
  // kód na vykonanie, ak ani podmienka1 ani podmienka2 nie sú splnené
}
```

- Vetvenie **switch**
```
switch (premenna) {
  case hodnota1:
    // kód na vykonanie, ak premenna == hodnota1
    break;
  case hodnota2:
    // kód na vykonanie, ak premenna == hodnota2
    break;
  default:
    // kód na vykonanie, ak sa premenna nezhoduje s žiadnou hodnotou
    break;
}
```

### Vlastnosti a rozdiely
- "**If**" a "**if-else**" sú základné vetvenia a umožňujú vyhodnotiť jednu podmienku.
- "**If else if else**" je vhodné použiť, keď je potrebné vyhodnotiť viacero podmienok za sebou a vykonať príslušný kód pre prvú splnenú podmienku.
- "**Switch**" je užitočný, keď je potrebné porovnávať hodnotu premennej s viacerými možnými hodnotami a vykonať príslušný kód pre zhodujúcu sa hodnotu.

### Porovnanie metód vetvenia v C++ a Jave
- Syntax a tvary vetvenia sú v oboch jazykoch podobné.
- V oboch jazykoch sa používa "if", "if-else" a "if-else if else" vetvenie.
- Vo výrazy s "switch" sú niektoré rozdiely. V C++ je povolené použiť hodnoty celých čísel a znakov, zatiaľ čo v Jave sa dajú použiť hodnoty typu celého čísla, znakov, enumu alebo reťazcov.
- V Jave je vyžadované použitie "break" po každom prípade v prípade "switch", ak chcete zabrániť prechodu na ďalšie prípady. V C++ je "break" voliteľné a môže sa použiť alebo vynechať.

[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
