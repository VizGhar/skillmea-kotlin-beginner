# 7.7 Interfaces

If an abstract class has all abstract functions and no attributes, it is often (not always) more appropriate to label it as `interface`. A class can inherit maximally from one class, but it can implement (more correctly stated: inherit from) any number of interfaces.

## 7.7.1 `rwx` example

In Linux, files have the permissions `read`, `write`, and `execute`. So whether they can be read, written to, or executed.

Write interfaces `Readable`, `Writeable`, and `Executable` with functions `read`, `write`, and `execute`.

Overcome the class `java.util.File` and name it `DocumentFile`. Which interfaces is it appropriate to implement in this class? Which functions should you overcome?

## 7.7.2 I don't need to override abstract

If an interface or abstract class inherits another interface or abstract class, this one does not have the obligation to implement its abstract functions.

1. In the `AlgorithmTester` class from the [7.6.3 Usage](07-06-abstract.md) exercise, remove the abstract function `runAlgorithm` and the code is fine again
2. Create your own interface called `Runnable` with a function `runAlgorithm` and the code is OK again

Create a concrete class `Concatenator`, which accepts a list of file paths as an argument and also implements the `Runnable` interface.
In the `runAlgorithm` function, print the contents of these files one under another.

## 7.7.3 Interface as an argument

Implement the `HttpCallback` class to print a general error message in case of failure and output on standard output in case of success.

Here are additional URLs for testing:
- https://dummyjson.com/users/1 - random user as JSON
- https://blockchain.info/ticker - Bitcoin price in several currencies as JSON
- https://pokeapi.co/api/v2/pokemon/pikachu - all information about Pikachu Pokémon as JSON format
- https://www.google.com/ - HTML Google page

```kt
import java.net.HttpURLConnection
import java.net.URI

interface HttpListener {
    fun onError()
    fun onSuccess(content: String)
}

fun invoke(url: String, callback: HttpListener) {
    try {
        val connection = URI(url).toURL().openConnection() as HttpURLConnection
        connection.requestMethod = "GET"
        connection.connectTimeout = 5000
        connection.readTimeout = 5000

        val responseCode = connection.responseCode
        if (responseCode == HttpURLConnection.HTTP_OK) {
            val content = connection.inputStream.bufferedReader().use { it.readText() }
            callback.onSuccess(content)
        } else {
            callback.onError()
        }

        connection.disconnect()
    } catch (e: Exception) {
        callback.onError()
    }
}

class HttpCallback : HttpListener {
    // TODO
}

fun main() {
    invoke("https://api.ipify.org/?format=json", HttpCallback())
}
```