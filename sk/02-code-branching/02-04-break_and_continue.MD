# 2.4 Break a Continue

`break` a `continue` nám umožňujú prerušiť cyklus, resp. preskočiť jeho
aktuálnu iteráciu.

## 2.4.1 Breakable Menu Screen

Uprav riešenie z úlohy [2.3.1 Menu Screen](02-03-while_and_do_while.MD) tak, aby
si namiesto používania podmienky v hlavičke `while` cyklu použil `break`

## 2.4.2 Sorter

Na štandardnom vstupe dookola načítavaj čísla.
1. Ak nebude zadané číslo, vypíš chybovú hlášku a `break`-ni cyklus
2. Ak zadané číslo nebude párne zavolaj `continue`
3. Ak zadané číslo bude párne vypíš ho na štandardný výstup

## 2.4.3 Primes

Napíš program, ktorý načíta celé číslo `n` a zistí, či je prvočíslo.

Teda iteruj čísla $`i \in \left[2, n-1\right]`$, ak bude číslo `n` deliteľné
niektorým z čísel `i` tak číslo `n` nie je prvočíslo.