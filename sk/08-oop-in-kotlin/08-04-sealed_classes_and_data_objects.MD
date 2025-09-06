# 8.4 Sealed triedy

Skús nanovo prepracovať úlohu, ktorú si videl v prezentácii. To
je najlepšia ukážka toho, na čo sa používajú sealed triedy a rozhrania.

## 8.4.1 Quadratic equation

Implementuj funkciu pre výpočet kvadratickej rovnice. Tá môže mať
viacero výstupov

- chyba ak je `determinant < 0`
- chyba ak je `a = 0`
- 1 výsledok ak je `determinant = 0`
- 2 výsledky aj je `determinant > 0`

Funkcia nech nevyhadzuje výnimky ale nech vracia `sealed` triedu
reprezentujúcu vyššie spomenuté možnosti.

## 8.4.2 Network communicator

Prepracuj úlohu [7.7.3 Rozhranie ako argument](../07-oop-basics/07-07-interface.MD)
tak, aby funkcia `invoke` neprijímala žiadne rozhranie. Namiesto toho nech rovno
vracia výsledok `Result` ako sealed triedu.

<details>

<summary>Pomôcka</summary>

```kt
fun invoke(url: String) : Result {
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

## 8.4.3 File Format (náročnejšie)

Väčšina binárnych súborov, napríklad aj obrázkové súbory
začína nejakou hlavičkou, podľa ktorej vieme zistiť, o aký súborový formát
sa jedná.

Napíš `sealed` triedu reprezentujúcu podporované obrázkové formáty. Napríklad
`JPG` a `BMP`. Obsah týchto tried nie je podstatný. Zároveň nech táto
sealed trieda obsahuje aj `data object Unknown` ak typ súboru nerozlíši.

Na štandardnom vstupe načítaj relatívnu cestu k súboru a vytvor správnu
inštanciu sealed triedy na základe hlavičky:

Pomôcky:
- súbor je typu JPG ak prvé byty majú hodnoty `FF D8`
- súbor je typu BMP ak prvé byty majú hodnoty `42 4D`
- súbor je typu PNG ak prvé byty majú hodnoty `89 50 4E 47 0D 0A 1A 0A`
- súbor môže byť typu SVG ak obsahuje text `<svg`

<details>

<summary>Ukážka pre JPG</summary>

```kt
fun isJpg(file: File): Boolean {
    if (!file.exists() || file.length() < 2) return false
    val bytes = file.readBytes()
    return bytes[0] == 0xFF.toByte() && bytes[1] == 0xD8.toByte()
}
```

</details>