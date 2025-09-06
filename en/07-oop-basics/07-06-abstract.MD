# 7.6 Abstract Classes

Abstract classes help write code that no one else accidentally uses incorrectly. It prevents direct instantiation of these classes and forces the implementation of abstract functions after an abstract class has been overridden.

## 7.6.1 Repair Open Types

Refactor tasks [7.4.1 Shapes](07-04-open_members_and_super.MD) and [7.4.2 Codes](07-04-open_members_and_super.MD) so that the basic classes `Shape2D` and `Cipher` are abstract classes as well as all their methods. Try to create an instance.

## 7.6.2 Map Provider

We've played with 2D maps before. Try to write an abstract class `MapProvider`, whose purpose is to return a 2D map as a two-dimensional array (or list) for a given `level`.

Specific implementations of this class can be:
1. `DummyMapProvider` - which returns a pre-created map for any `level`
2. `FileMapProvider` - which loads the map from file `<level>.txt`
3. `GenerateMapProvider` - which generates a random map (extremely challenging task)

## 7.6.3 Usage

Implement this abstract class so that the function `runAlgorithm` starts searching for number `k` in a sorted array of size `n`. On standard output, print the first index at which this element is located.

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

Then call the function `runTestWithReport` to find out how fast your algorithm is. Note that the array is SORTED, so you can write a faster algorithm:

```kt
class IndexFinder(val list: List<Int>, val item: Int) : AlgorithmTester() {
    override fun runAlgorithm() {
        println(list.indexOf(item))
    }
}
```

Try this algorithm on an array of at least 10,000,000 elements:

```kt
fun main() {
    val list = List(10_000_000) { kotlin.random.Random.nextInt() }.sorted()
    val item = list.random()

    IndexFinder(list, item).runTestWithReport()
}
```