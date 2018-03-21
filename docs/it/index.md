[Select Language](../)
# 1.Elenco  
## 1.1 Tasti statici
Nessun calcolo necessario, verificare direttamente con la chiave.
## 1.2 Tasti dinamici
Genera chiavi per espressioni, quindi verifica.
# 2.scoppiare  
## 2.1 Modalità Dict
Usa il dizionario delle chiavi per far esplodere il settore.
## 2.2 Aumentare la modalità

- `00` `01`   ……  `FE` `FF` Si trova per byte non cifrato.
- `u0` `u1` `u2` `u3` Supporta i 4 byte di UID.
- Un BLANK significa che genererà le chiavi con aumento su questo byte.

``` 
Esempio 1：
Ingresso
00 12 34 56 78 __
creare
00 12 34 56 78 00
00 12 34 56 78 01
00 12 34 56 78 02
...
00 12 34 56 78 FE
00 12 34 56 78 FF
Totale 256 chiavi
```

```
Esempio 2：
Attualmente, UID is 99 88 77 66
Ingresso
__ u0 u1 u2 u3 __
creare
00 99 88 77 66 00
00 99 88 77 66 01
00 99 88 77 66 02
...
FF 99 88 77 66 FE
FF 99 88 77 66 FF
Totale 65536 chiavi
```
