# 3.1 Funkcie - základy

Na praktických úlohách si môžeš otestovať základné tvary funkcií
v Kotline. Funkcie obvykle prevádzajú vstupy na výstupy, avšak
zápisov existuje samozrejme viac.

Zadania budú vyžadovať len napísanie funkcií. Samozrejme, testovací kód napíš sám.

## 3.1.1 Bez vstupu a výstupu

Napíš funkciu s názvom menu, ktorá na štandardný výstup len vypíše obsah hlavného menu
podľa úlohy [2.3.1 Menu Screen](../02-code-branching/02-03-while_and_do_while.MD). Táto funkcia
je určená len na výpis, teda bude maličká.

## 3.1.2 So vstupom, bez výstupu

Napíš funkciu, do ktorej pošleš dve celé čísla ako rozmer 2D priestoru. Podľa
podmienok popísaných v úlohe [2.5.3 Boundary checker](../02-code-branching/02-05-logic_operators.MD)
v cykle načítavaj súradnice `x` a `y` kým nebudú splnené všetky podmienky.

Keď budú podmienky splnené vypíš text:
> Načítaná súradnica je [`x`, `y`]

## 3.1.3 Bez vstupu s výstupom

Napíš funkciu s názvom `readPrime`, ktorej úlohou je získať prvočíslo zo štandardného
vstupu. Táto funkcia nesmie vrátiť iné číslo ako prvočíslo (bude obsahovať cyklus s
validáciou).


## 3.1.4 Bez vstupu s výstupom 2

Napíš funkciu s názvom `consoleReadYn`, ktorej úlohou je
1. vypísať text `Do you want to continue? [Y/n]`
2. vrátiť `true` ak načítaný text je `Y` alebo `y`
3. vrátiť `false` ak načítaný text nebude `Y` ani `y`

## 3.1.5 So vstupom a s výstupom

Uprav úlohu 3.1.2. Do funkcie posielaj okrem šírky a výšky aj `x` a `y` súradnice.
Z funkcie vráť `true` ak `x` a `y` spadajú do priestoru definovanej výšky a šírky.
Cyklus pre overenie správnosti vstupu vytiahni do funkcie `main` napríklad nasledovne:

```kt
fun main() {
    // ... get width, height
    while(true) {
        // ... get x, y
        if (isValid(width, height, x, y)) {
            // output
            break
        }
    }
}
```