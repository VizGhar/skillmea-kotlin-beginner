# 2.5 Logické operátory

Použitím logických operátorov vieš spojiť 2 `if`-y do jedného!

## 2.5.1 Test ||

Na štandardnom vstupe načítaj číslo `n` (`n < 1000`). Vypíš všetky čísla menšie
ako `n` také, ktoré sú deliteľné číslom 5 alebo 11.

## 2.5.2 Test &&

Na štandardnom vstupe načítaj číslo `n` (`n < 1000`). Vypíš všetky čísla menšie
ako `n` také, ktoré sú deliteľné číslom `5` a zároveň obsahuje v desiatkovom
zápise aspoň jednu trojku.

## 2.5.3 Boundary checker

Na štandardnom vstupe načítaj čísla `width` a `height` teda šírku a výšku 2D
priestoru. Následne v nekonečnom cykle načítavaj hodnoty `x` a `y`.

Začiatočný bod v tomto 2D priestore má súradnicu `[0, 0]`

1. Ak bod na súradnici `[x, y]` bude mimo 2D priestoru, vypíš chybu
2. Ak bod na súradnici `[x, y]` bude v 2D priestore, vypíš hlášku s pochvalou

_Ukážka vstupov a výstupov:_
```
5 4        // sirka je 5 vyska je 4
0 0 OK     // 0 0 spada do intervalov <0, 5] a <0, 4]
5 0 CHYBA  // x nespada do intervalu <0, 5]
0 4 CHYBA  // y nespada do intervalu <0, 4]
3 3 OK     //
-1 0 CHYBA // x nespada do intervalu <0, 5]
```