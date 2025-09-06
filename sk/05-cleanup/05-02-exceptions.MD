# 5.2 Výnimky

Teraz poďme sami zhadzovať vlastnú aplikáciu :)

## 5.2.1 Bloček

Napíš funkciu `calculatePrice(quantity: Int, price: Double)`, ktorá
vyráta výslednú cenu produktov. Každý tretí produkt nech je zadarmo.

- `quantity` - počet produktov
- `price` - cena jedného produktu

Funkciu zhoď pomocou `IllegalArgumentException` ak budú vstupy nevalidné.

## 5.2.2 Objednávka

Napíš triedu reprezentujúcu objednávku. Nech obsahuje aspoň 2 atribúty.
1. `status` - stav objednávky ako číslo
2. `id` - identifikátor objednávky - napríklad `String`

`status` nadobúda jednu z hodnôt
- `1` - vytvorená - povolené ďalšie stavy - 2 a 4
- `2` - spracovaná - povolené ďalšie stavy - 3 a 4
- `3` - expedovaná - povolené ďalšie stavy - 4
- `4` - zrušená - povolené ďalšie stavy - žiadne

Trieda bude mať aj funkciu pre zmenu stavu objednávky. Ak túto funkciu zavoláš
s nesprávnou hodnotou, vyhoď `IllegalStateException`

## 5.2.3 Out Of Bounds

Napíš funkciu, ktorá prijíma výšku a šírku 2D plochy ako aj `X` a `Y` súradnicu na tejto ploche.
Ak sa bude bod `[X,Y]` mimo plochy vyhoď vlastnú výnimku, alebo nájdi nejakú vhodnú.