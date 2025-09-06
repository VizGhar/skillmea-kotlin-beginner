# 6.2 Polia

## 6.2.1 Jednorozmerné pole
Na štandardnom vstupe
1. načítaj číslo `n`
2. `n` x načítaj riadok s číslom
3. načítaj číslo `k` a `m` 

V zozname načítaných čísel následne zmeň všetky čísla s hodnotou `k`
na hodnotu `m` a pole vypíš na štandardný výstup.

## 6.2.2 Sčítanie matíc
Dvojrozmerné pole je jednoducho pole polí. Jedno také pole vie vyzerať
nasledovne:

```kt
val pole1 = arrayOf(
    arrayOf(1, 2),
    arrayOf(3, 4),
    arrayOf(5, 6)
)
```

Na štandardnom vstupe
1. načítaj výšku `h` a šírku `w` 2D poľa
2. `h` x `w` hodnôt reprezentujúcich prvé 2D pole
3. `h` x `w` hodnôt reprezentujúcich druhé 2D pole

Na štandardnom výstupe vypíš výsledok súčtu týchto dvoch polí.

| Ukážka vstupu                                                                          | Ukážka výstupu                        |
|----------------------------------------------------------------------------------------|---------------------------------------|
| ```2 2```<br/>```1 2```<br/>```3 4```<br/>```7 3```<br/>```2 8```                      | ```8 5```<br/>```5 12```              |
| ```2 4```<br/>```1 2 15 5```<br/>```13 6 21 8```<br/>```3 2 8 8```<br/>```9 18 5 22``` | ```4 4 23 13```<br/>```22 24 26 30``` |


## 6.2.3 Map Editor
Vytvorte jednoduchý editor pre 2D ASCII hru.

1. Na štandardnom vstupe načítaj rozmer hracej plochy. Predvolený znak na tejto ploche je `.`
2. V cykle
   1. načítaj `X` a `Y` pozíciu, kam chceš umiestniť predmet
   2. načítaj `znak`, ktorý chceš umiestniť na pozíciu `[X, Y]`
   3. vykresli zatiaľ navrhnutú mapu


| Ukážka vstupu                                                               | Ukážka výstupu<br/>(len posledná iterácia) |
|-----------------------------------------------------------------------------|---------------------------------------|
| ```3 3```<br/>```0 0 /```<br/>```2 0 \ ```<br/>```0 2 \ ```<br/>```2 2 /``` | ```/.\ ```<br/>```...```<br/>```\./``` |
