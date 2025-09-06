# 4.4 Funkcie inštancie

Okrem prenášania dát dokážu objekty mať aj nejaké správanie. To
si vyskúšame na nasledujúcich cvičeniach.

## 4.4.1 Čas

Napíš triedu `Time` reprezentujúcu čas na hodinkách aj s týmito funkciami:

1. `addMinutes(m: Int)`: vráti nový čas posunutý o `m` minút dopredu (správne pretečie cez 60 min)
2. `toString()`: vráti čas vo formáte `HH:MM`, napr. "09:05"
3. `isBefore(other: Time)`: zistí, či je aktuálny čas pred iným časom
4. `totalMinutes()`: vráti počet minút od polnoci
5. `diff(other: Time)`: vráti rozdiel medzi časmi v minútach (ako celé číslo)

## 4.4.2 Zlomky

Napíš triedu reprezentujúcu zlomok. Teda obsahuje čitateľ a menovateľ.

Napíš v nej funkcie pre
1. sčítanie zlomkov
2. odčítanie zlomkov
3. prevod zlomku do základného tvaru
4. pričítanie celého čísla k zlomku
5. odčítanie celého čísla od zlomku

Tieto operácie nech vždy vrátia novú inštanciu zlomku (čitateľ a menovateľ
musia byt `val`)

