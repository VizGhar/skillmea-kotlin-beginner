# 1.4 Štandardný vstup a výstup

Zaujímať nás bude hlavne načítavanie zo štandardného vstupu. Obe úlohy odporúčam revidovať, keď
absolvuješ tému _1.5 String templates_

## 1.4.1 Interaktívny pozdrav

Niekedy sa pri konzolových aplikáciách stretneš s interaktivitou, teda aplikácia s tebou komunikuje.
Napríklad pri volaní `sudo apt-get upgrade` (Ubuntu) sa ťa program `apt-get` môže opýtať:

```
Do you want to continue? [Y/n]
```

Kurzor v tejto aplikácii zostane na tom istom riadku a čaká na klávesu `Y` alebo `n`.
Po zadaní program pokračuje.

Skús vytvoriť podobnú interaktívnu aplikáciu:

1. Na štandardnom výstupe vypíš text: _"Zadaj svoje meno: "_, kurzor musí ostať za týmto textom
2. Na štandardnom vstupe načítaj _meno a priezvisko_ do jednej premennej s názvom `meno`
3. Na štandardnom výstupe vypíš text _"Vitaj `meno`"_, kde `meno` je hodnota premennej z bodu 2

## 1.4.2 Chyták

1. Na prvom riadku načítaj dve celé čísla `X` a `Y`
2. Na druhom riadku načítaj názov postavičky do premennej `meno`. Napríklad _"Jozko Mrkvicka"_
3. Na treťom riadku vypíš text _"`meno` sa nachádza na súradnici `X`, `Y`"_, kde `meno`, `X` a `Y`
sú premenné z bodov 1 a 2

_Poznámka:_ Daj si pozor, kde sa nachádza "kurzor" po načítaní premenných `X` a `Y`
