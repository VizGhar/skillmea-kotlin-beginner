# 7.6 Abstraktné triedy

Abstraktné triedy pomáhajú písať kód tak, aby ho niekto iný náhodou
nepoužil nesprávne. Zakazuje priamu inštanciáciu týchto tried a po
prekonaní abstraktnej triedy núti implementovať abstraktné funkcie.

## 7.6.1 Oprava open tried

Prepracuj úlohy [7.4.1 Tvary](07-04-open_members_and_super.MD) a [7.4.2 Šifry](07-04-open_members_and_super.MD)
tak, aby základné triedy `Shape2D` a `Cipher` boli abstraktné triedy ako aj všetky ich metódy.
Skús vytvoriť inštancie.

## 7.6.2 Map provider

S 2D mapami sme sa už hrali. Skús napísať abstraktnú triedu `MapProvider`, ktorej úlohou
je vrátiť 2D mapu ako dvojrozmerné pole (alebo zoznam) pre daný `level`.

Konkrétne implementácie tejto triedy môžu byť:
1. `DummyMapProvider` - ktorý pre akýkoľvek `level` vráti natvrdo vytvorenú mapu
2. `FileMapProvider` - ktorý stiahne mapu zo súboru `<level>.txt`
3. `GenerateMapProvider` - ktorý vygeneruje náhodnú mapu (extrémne náročné zadanie)

## 7.6.3 Použitie

Implementuj túto abstraktnú triedu tak, aby v novej triede
funkcia `runAlgorithm` spustila vyhľadávanie čísla `k` v zoradenom
poli veľkosti `n`. Na štandardnom výstupe vypíše prvý index na
ktorom sa táto položka nachádza.

```kt
abstract class AlgorithmTester {

    abstract fun runAlgorithm()

    fun measureTime(): Long {
        val startTime = System.nanoTime()
        runAlgorithm()
        val endTime = System.nanoTime()
        return endTime - startTime
    }

    fun runTestWithReport() {
        val timeNano = measureTime()
        println("Execution time: ${timeNano / 1_000_000} ms")
    }
    
}
```

Následne zavolaj funkciu `runTestWithReport`, aby si zistil aký rýchly
je tvoj algoritmus. Pripomínam, že pole je ZORADENÉ, preto sa dá napísať
rýchlejší algoritmus ako:

```kt
class IndexFinder(val list: List<Int>, val item: Int) : AlgorithmTester() {
    override fun runAlgorithm() {
        println(list.indexOf(item))
    }
}
```

Algoritmus skúšaj na poli o veľkosti aspoň 10.000.000 miliónov
položiek:

```kt
fun main() {
    val list = List(10_000_000) { kotlin.random.Random.nextInt() }.sorted()
    val item = list.random()

    IndexFinder(list, item).runTestWithReport()
}
```