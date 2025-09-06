# 7.4 Otvorené atribúty a funkcie

Zatiaľ sme mali dosť zviazané ruky. Jedinú možnosť, ktorú sme
pri dedení mali k dispozícii, bol v podstate copy paste celého
správania nejakej triedy. S otvorenými atribútmi a funkciami (alebo
členmi - angl. members) už vieme tieto "copy-paste"-y upravovať.

## 7.4.1 Tvary

1. Vytvor triedu `Shape2D` bez atribútov
2. V triede `Shape2D` vytvor funkciu `perimeter` (obvod), ktorá vracia `Double`
3. V triede `Shape2D` vytvor funkciu `area` (obsah), ktorá vracia `Double`
4. Vytvor triedu `Circle`, ktorá rozširuje `Shape2D`
5. V triede `Circle` správne implementuj funkcie `perimeter` a `area`
6. Podobne vytvor a implementuj `Rectangle`

## 7.4.2 Šifry

1. Vytvor triedu `Cipher` bez atribútov
2. V triede `Cipher` vytvor funkciu `encode(text)`, ktorá vracia zašifrovaný text
3. V triede `Cipher` vytvor funkciu `decode(text)`, ktorá vracia dešifrovaný text
4. Vytvor a implementuj triedu `SubstitutionCypher`, teda substitučnú šifru, ktorá rozširuje `Cipher`
5. Vytvor a implementuj triedu `ShiftCypher`, teda posuvnú šifru, ktorá rozširuje `Cipher`

Sám si navrhni detaily týchto tried.