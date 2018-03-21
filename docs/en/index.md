# 1.List  
## 1.1 Static Keys
No need calculation, verify with the key directly.
## 1.2 Dynamic Keys
Generate keys by expressions, then verify.
# 2.Burst  
## 2.1 Dict Mode
Use dictionary of keys to burst the sector.
## 2.2 Increase Mode

- `00` `01`   ……  `FE` `FF` Stands for unchanged byte.  
- `u0` `u1` `u2` `u3` Stand for the 4 bytes of UID.
- A BLANK means it will generate keys with increasing on this byte.

``` 
Example 1：
Input
00 12 34 56 78 __
Generate
00 12 34 56 78 00
00 12 34 56 78 01
00 12 34 56 78 02
...
00 12 34 56 78 FE
00 12 34 56 78 FF
Total 256 Keys
```

```
Example 2：
Currently, UID is 99 88 77 66
Input
__ u0 u1 u2 u3 __
Generate
00 99 88 77 66 00
00 99 88 77 66 01
00 99 88 77 66 02
...
FF 99 88 77 66 FE
FF 99 88 77 66 FF
Total 65536 Keys
```
