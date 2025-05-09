# 7.7 Rozhrania

Ak má abstraktná trieda všetky funkcie abstraktné a nemá žiadne
atribúty, tak je často (nie vždy) vhodnejšie označiť ju ako
`interface`. Trieda dedí maximálne od jednej triedy, ale môže dediť
(správnejšie povedané implementovať) od neobmedzeného množstva
rozhraní.

## 7.7.1 `rwx` ukážka

V Linuxe majú súbory zapnuté alebo vypnuté príznaky `read`, `write` a
`execute`. Teda či sa dajú čítať, či sa do nich dá zapisovať, alebo či
sa dajú spúšťať.

Napíš rozhrania `Readable`, `Writeable` a `Executable` s funkciami
`read`, `write` resp. `execute`.

Prekonaj triedu `java.util.File` a nazvi ju `DocumentFile`. Aké
rozhrania je vhodné v tejto triede implementovať? Ktoré funkcie
je vhodné prekonať?

## 7.7.2 Nemusím prekonávať abstract

Ak od rozhrania, alebo abstraktnej triedy dedí iné rozhranie alebo
abstrakná trieda, táto nemá povinnosť implementovať jej abstraktné
funkcie.

1. V triede `AlgorithmTester` z úlohy [7.6.3 Použitie](07-06-abstract.MD)
   vymaž abstraktnú funkciu `runAlgorithm` a kód ti sčervená
2. Vytvor tvoje vlastné rozhranie s názvom `Runnable` a funkciou `runAlgorithm`
   a kód je znova OK

Vytvor aj konkrétnu triedu `Concatenator`, ktorá prijme ako argument
zoznam ciest k súborom a tiež implementuje rozhranie `Runnable`.
Vo funkcii `runAlgorithm` vypíš obsah týchto súborov pod sebou.

## 7.7.3 Rozhranie ako argument

Implementuj triedu `HttpCallback` aby v prípade chyby vypísala
všeobecnú chybu a v prípade úspechu vypísala výstup na štandardný
výstup.

Tu sú ďalšie url na testovanie:
- https://dummyjson.com/users/1 - náhodný používateľ ako JSON
- https://blockchain.info/ticker - cena bitcoinu vo viacerých menách ako JSON
- https://pokeapi.co/api/v2/pokemon/pikachu - všetky informácie o
Pikachu Pokémonovi v JSON formáte
- https://www.google.com/ - HTML stránky Google

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