# 4.2 Triedy a objekty

Teraz už vieš, ako vytvoriť triedu a z nej objekty. Triedy a objekty
sú vždy vo vzťahu `1-n`. Teda `1` trieda dokáže mať `0` a viac inštancií
nazývaných objekty.

## 4.2.1 Pozícia

Toto je jedna z najklasickejších tried, na ktorej chápeme základy.
Vytvor triedu s názvom `Position`, ktorá bude mať atribúty `x` a `y`.

Vo funkcii `main` vytvor 3 inštancie tejto triedy a nastav im rôzne
hodnoty. Následne tieto hodnoty aj vypíš na štandardný výstup.

## 4.2.2 Adresa

Ak tvoja aplikácia pracuje s databázami, často bude opisovať používateľov
aplikácie. Jednou z takýchto informácií je aj adresa. Ak by si ju držal v
jednom textovom poli, ľahko by si narazil na limity pri filtrovaní, či
radení položiek.

Vytvor teda triedu `Address` reprezentujúcu fyzickú adresu. Vytvor jej dve
inštancie. Jedna nech representuje teba, druhá tvojho kamaráta. Napíš aj
funkciu na krajší výpis adresy.

## 4.2.3 Inception

Napíš triedu `User` s nasledovnými poliami
1. `username: String`
2. `email: String`
3. `pass: String`
4. `address: Address`

Teraz vidíš, že jeden objekt dokáže obsahovať ďalší objekt.
