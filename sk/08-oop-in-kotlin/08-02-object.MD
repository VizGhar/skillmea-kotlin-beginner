## 8.2 `object`

`object` je označenie pre singleton triedy. Sú to také triedy, ktoré majú
práve jednu jedinú inštanciu. Novú inštanciu "triedy" s označením `object`,
vytvoriť nevieš. Pretože už existuje a to priamo pri jej definícii.

## 8.2.1 Global `object`

Veľmi ľahko sa môže stať, že zabudneš názov nejakej globálnej funkcie.
Preto je niekedy vhodné tieto funkcie napchať do jedného objektu.

Vytvor `object Network` v samostatnom `.kt` súbore, v ktorom budeš
definovať konfiguračné hodnoty a funkcie pre tvoju aplikáciu.

V tomto objekte vytvor tieto premenné a funkcie:
- privátna premenná `BASE_URL` s hodnotou `"https://dummyjson.com/"`
- privátna konštanta `TIMEOUT` s hodnotou `5000`
- public funkcia `setBaseUrl(path: String)`, ktorá nastaví `BASE_URL`, ak je valídna (`https://.../`)
- public funkcia `get(path: String)`, ktorá vráti url zloženú z `BASE_ULR + path`

Otestuj fungovanie a použitie tohto objektu.

## 8.2.2 Rozhranie ako argument 2

Uprav úlohu [7.7.3 Rozhranie ako argument](../07-oop-basics/07-07-interface.MD) tak
aby si neimplementoval `HttpListener` ako samostatnú triedu,
ale skús použiť `object`:

```kt
fun main() {
    invoke(
        "https://api.ipify.org/?format=json",
        object : HttpListener {
            // ...
        })
}
```

Takto môžeš pre každé volanie funkcie `invoke` definovať iné správanie
bez potreby vytvárať ďalšie a ďalšie triedy.