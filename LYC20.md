# 20. Programovací jazyk - objektovo orientované programovanie
deklarácia triedy, jej atribúty a úrovne prístupu, pojmy konštruktor, deštruktor, metóda, preťažovane, dedičnosť, štruktúrované, objektovo orientované a komponentové programovanie

### Deklarácia triedy
- V Jave sa deklaruje trieda pomocou kľúčového slova class. Syntax pre deklaráciu triedy je nasledovná:
```
[modifikátory] class NazovTriedy {
  // atribúty, konštruktory, metódy
}
```

### Atribúty triedy
- Atribúty sú premenné, ktoré slúžia na uchovávanie dát v rámci triedy.
- Deklarujú sa v tele triedy a môžu mať rôzne úrovne prístupu (public, private, protected, bez modifikátoru).
- Príklad deklarácie atribútu:
```
public class MojaTrieda {
    private int cislo;
    public String meno;
}
```

### Úrovne prístupu
- **public**: Atribút alebo metóda je prístupná zo všetkých častí programu.
- **private**: Atribút alebo metóda je prístupná iba zvnútra tej istej triedy.
- **protected**: Atribút alebo metóda je prístupná zvnútra triedy a jej podtried.
- **Bez modifikátora**: Atribút alebo metóda je prístupná v rámci rovnakej balíka (package).

### Konštruktor
- Konštruktor je špeciálna metóda, ktorá sa volá pri vytváraní inštancie triedy (objektu).
- Slúži na inicializáciu atribútov triedy.
- Má rovnaký názov ako trieda a nemá žiadny návratový typ.
- Príklad deklarácie konštruktora:
```
public class MojaTrieda {
    private int cislo;

    public MojaTrieda(int cislo) {
        this.cislo = cislo;
    }
}
```

### Deštruktor
- V Jave nie je explicitný deštruktor ako v niektorých iných jazykoch (napr. C++).
- Java má automatické garbage collection, čo znamená, že sa stará o uvoľňovanie pamäte, keď objekt už nie je potrebný.

### Metóda
- Metóda je blok kódu, ktorý vykonáva určitú operáciu alebo vracia hodnotu.
- Môže mať parametre a návratový typ (ak nevracia hodnotu, používa sa void).
- Príklad deklarácie metódy:
```
public class MojaTrieda {
    private int cislo;

    public void vypisCislo() {
        System.out.println(cislo);
    }
}
```

### Preťažovanie (overloading)
- Preťažovanie umožňuje mať viacero metód s rovnakým názvom, ale s odlišnými parametrami.
- Metódy sa rozlíšia podľa počtu alebo typu parametrov.
- Príklad preťažovania metód:
```
public class MojaTrieda {
    public void vypis(int cislo) {
        System.out.println(cislo);
    }

    public void vypis(String retazec) {
        System.out.println(retazec);
    }
}
```

### Dedičnosť
- Dedičnosť je princíp objektovo orientovaného programovania, ktorý umožňuje vytváranie hierarchie tried.
- Podtriedy (dedičné triedy) môžu dediť atribúty a metódy od nadtriedy (rodičovej triedy).
- Príklad dedičnosti:
```
public class RodicovaTrieda {
    // atribúty a metódy
}

public class Podtrieda extends RodicovaTrieda {
    // atribúty a metódy špecifické pre podtriedu
}
```

### Štruktúrované, objektovo orientované programovanie
- Štruktúrované programovanie sa zameriava na skladanie programu z procedúr a funkcíí.
- Objektovo orientované programovanie (OOP) sa zameriava na modelovanie sveta pomocou objektov a interakcie medzi nimi.
- Komponentové programovanie sa zameriava na vytváranie programov pomocou nezávislých a znovupoužiteľných komponentov.
- Java je objektovo orientovaný programovací jazyk, ktorý podporuje princípy OOP a umožňuje vytvárať triedy, objekty, dedičnosť a ďalšie OOP koncepty.

[1](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC/) | [2](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC2/) | [3](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC3/) | [4](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC4/) | [5](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC5/) | [6](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC6/) | [7](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC7/) | [8](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC8/) | [9](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC9/) | [10](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC10/) | [11](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC11/) | [12](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC12/) | [13](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC13/) | [14](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC14/) | [15](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC15/) | [16](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC16/) | [17](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC17/) | [18](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC18/) | [19](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC19/) | [20](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC20/) | [21](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC21/) | [22](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC22/) | [23](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC23/) | [24](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC24/) | [25](https://jesuschrist69.github.io/maturitne-otazky-SPSIT-KNM-2023/LYC25/)
