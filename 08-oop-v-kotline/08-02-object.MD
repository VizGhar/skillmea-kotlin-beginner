## 8.2 `object`

`object` je označenie pre singleton triedy. Sú to také triedy, ktoré majú
práve jednu jedinú inštanciu. Novú inštanciu "triedy" s označením `object`,
vytvoriť nevieš. Pretože už existuje a to priamo pri jej definícii.

## 8.2.1 Global `object`

## 8.2.3 Rozhranie ako argument 2

Uprav úlohu [7.7.3 Rozhranie ako argument](../07-oop-zaklady/07-07-interface.MD) tak
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