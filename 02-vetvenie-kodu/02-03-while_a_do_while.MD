# 2.3 While a Do-while

Pomocou kľúčového slovíčka `if` dokážeš dať svojej aplikácii základnú logiku. Poďme na to

## 2.3.1 Menu Screen

Množstvo hier sa začína uvítacou Menu obrazovkou s možnosťami ako

- [N]ew Game
- [L]oad Game
- [E]xit Game

Napíš program, ktorý čaká, kým používateľ nezadá jedno z písmen
N/L/E. Ak zadá správne písmeno, vypíš, ktorú možnosť zvolil a ukonči
prigram. Ak zadá nesprávne písmeno/text, vypíš chybovú hlášku a zopakuj
program.

## 2.3.2 8th Wonder

Warren Buffet nazval zložený úrok ôsmy div sveta. Narážal na postupne
rastúce úroky v investíciách. Keď napríklad vložíš na investičný účet
s výnosom 10% 1000EUR, tak táto investícia v priebehu rokov rastie
nasledovne:

1. 1000 + 100
2. 1100 + 110
3. 1210 + 121
4. 1331 + 133.1
5. 1464.1 + 146.41
6. ...

Zisti, koľko rokov bude trvať aby zo vstupnej investície 10000EUR získal
investor milión.

## 2.3.3 Do-while

Napíš program, ktorý vygeneruje náhodné celé číslo od 1 do 10 a potom
opakovane pýta používateľa, aby hádal toto číslo. Program pokračuje, kým
používateľ neuhádne správne číslo. Na konci vypíše, koľko pokusov používateľ
potreboval.

Tu máš základ:

```kt
import kotlin.random.Random

fun main() {
    val target = Random.nextInt(1, 11) // náhodné číslo od 1 do 10

    do {

    } while (true)

    println("Správne! Počet pokusov: ???")
}
```

**Podmienka:** Použi cyklus do-while na opakovanie zadávania vstupu.

## 2.3.4 Počet cifier

Do celočíselnej premennej načítaj číslo zo štandardného vstupu
(musí to byť číslo). Na štandardný výstup vypíš, koľko má cifier.