# 3.4 Named arguments

Nech hlavička tvojej funkcie vyzerá nasledovne:
```kt
fun createWelcomeMessage(
    name: String,
    greeting: String = "Ahoj",
    punctuation: String = "!",
    uppercase: Boolean = false,
    emoji: String = ""
): String
```

Výstupom tejto funkcie bude napríklad text:
> AHOJ JANKO! 👋

Vyskúšaj si použitie takejto funkcie

## 3.4.1 ASCII Frame

Napíš vlastnú funkciu pre vypisovanie textu v rámčeku. Ak bude vstupný text
_"Hello"_, výstup s ostatnými predvolenými hodnotami bude vyzerať nasledovne:

```
#########
#       #
# Hello #
#       #
#########
```

Meniť by si, okrem textu, mal vedieť:
1. hrúbku rámčeka (predvolene `1`)
2. vnútorný padding (predvolene `1`)
3. znak reprezentujúci rámček (predvolene `#`)