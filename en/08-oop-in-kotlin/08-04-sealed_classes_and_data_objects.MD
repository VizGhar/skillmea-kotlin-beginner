# 8.4 Sealed Classes

Try to rework the task you saw in the presentation. This is the best example of how sealed classes and interfaces are used.

## 8.4.1 Quadratic Equation

Implement a function for calculating a quadratic equation. It can have multiple outputs:

- error if `determinant < 0`
- error if `a = 0`
- 1 result if `determinant = 0`
- 2 results if `determinant > 0`

The function should not throw exceptions but return a sealed class representing the above options.

## 8.4.2 Network Communicator

Rewrite task [7.7.3 Interface as Argument](../07-oop-basics/07-07-interface.MD) so that the `invoke` function does not accept any interface. Instead, it should directly return a result sealed class.

<details>

<summary>Help</summary>

```kt
fun invoke(url: String): Result {
    try {
        val connection = URI(url).toURL().openConnection() as HttpURLConnection
        connection.requestMethod = "GET"
        connection.connectTimeout = 5000
        connection.readTimeout = 5000

        val responseCode = connection.responseCode
        if (responseCode == HttpURLConnection.HTTP_OK) {
            val content = connection.inputStream.bufferedReader().use { it.readText() }
            return Result...(content)
        } else {
            return Result...
        }

        connection.disconnect()
    } catch (e: Exception) {
        return Result...
    }
}
```

</details>

## 8.4.3 File Format (more challenging)

Most binary files, such as image files, start with some kind of header that allows us to determine which file format is being used.

Write a sealed class representing supported image formats, for example `JPG` and `BMP`. The contents of these classes are not important. Meanwhile, this sealed class should also include a `data object Unknown` if the file type cannot be determined.

On standard input, read a relative path to a file and create an instance of the sealed class based on the header:

Helps:
- A file is of type JPG if the first bytes have values `FF D8`
- A file is of type BMP if the first bytes have values `42 4D`
- A file is of type PNG if the first bytes have values `89 50 4E 47 0D 0A 1A 0A`
- A file may be of type SVG if it contains text `<svg>`

<details>

<summary>Example for JPG</summary>

```kt
fun isJpg(file: File): Boolean {
    if (!file.exists() || file.length() < 2) return false
    val bytes = file.readBytes()
    return bytes[0] == 0xFF.toByte() && bytes[1] == 0xD8.toByte()
}
```

</details>