# 7.3 Modifikátory prístupu

Nie všetko z našej nadtriedy chceme vidieť v našej zdedenej triede.
K tomu nám poslúžia práve modifikátory prístupu.

## 7.3.1 Substitution cypher - privátny atribút

Napíš triedu pre zakódovanie a dekódovanie substitučnej šifry.
Kľúčom bude vždy text, ktorý obsahuje všetky písmená `a-z` v rôznom poradí.

V prípade kľúča _"xyzabcdefghijklmnopqrstuvw"_ bude písmeno `A` mapované na písmeno `X`,
písmeno `B` na písmeno `Y` a podobne (pozri celé mapovanie nižšie)

```
xyzabcdefghijklmnopqrstuvw
abcdefghijklmnopqrstuvwxyz
```

1. Vytvor triedu `SubstitutionCypher` s privátnym atribútom `key`
2. Implementuj funkciu na šifrovanie `encode`, ktorá používa skrytý kľúč
3. Implementuj funkciu na dešifrovanie `decode`, ktorá používa skrytý kľúč

Myslíš, že by bolo vhodné tento `key` držať ako public atribút?

## 7.3.2 Level - privátna funkcia

Vytvor triedu, ktorá drží 2D mapu tvojej hry `map` a pozíciu postavičky `x` a `y`.
Vytvor v nej funkcie:

1. `look(direction: Int): Char?`, ktorá zistí, aký predmet sa nachádza smerom `direction` od tvojej postavičky
2. `go(direction: Int): Unit`, ktorá sa pokúsi posunúť postavičku smerom `direction`

Direction môže mať hodnoty 0-3 reprezentujúce smery `LEFT`, `TOP`, `RIGHT`, `BOTTOM`

Obe tieto funkcie môžu chcieť kontrolovať, či náhodou nechceš získať objekt mimo hracej plochy.
Odporúčam teda prichystať si aj skrytú privátnu funkciu na kontrolu okrajov - `inBounds(x: Int, y: Int): Boolean`

## 7.3.3 File private

Zopakuj zadanie 7.3.1, ale nevytváraj triedu. Namiesto toho vytvor nový súbor s public funkciami
`encode` a `decode`. `key` je natvrdo nastavený v tomto súbore a, samozrejme, privátny.