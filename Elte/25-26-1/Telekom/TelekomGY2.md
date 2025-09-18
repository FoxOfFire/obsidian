# telekom gy 1

bit paritásokkal való bíbelődés

| 1 | 2 | 3 | 4 |Check|
|---|---|---|---|-----|
| 1 | 0 | 1 | 1 |  1  |
| 1 | 0 | 0 | 1 |  0  |
| 0 | 0 | 0 | 1 |  1  |
|---|---|---|---|     |
| 0 | 0 | 1 | 1 |     |

## CRC
>
> ### Egyszerű példa
>
> Üzenet: 1101 (x^3+x^2+1)
> Generátor polinom: 11 (x+1)
> xgM(x): 11010
>
> Küldő kiszámítja az osztás maradékát → pl. 1.
> Az átküldött üzenet: 11011 (eredeti üzenet + CRC).
> Vevő elosztja 11011-t 11-gyel.
>
> Ha maradék = 0 → jó.
>
> Ha ≠ 0 → hiba.
>
## feladatok
>
> ### 1
>
> A 7 bites kódszavak alkotják a kódkönyvtárat. Adjunk hozzá egy paritásbitet,
> ami 1 ha a kódszóban lévő egyesek száma páratlan és 0 ha páros.
>
> Adj példát!
> Mekkora ezen kód Hamming-távolsága?
> Mennyi egyszerű és milyen hosszú löketszerű hibát képes kezelni?
>
> #### megoldás
>
> LIBA:(
> konkrétan fogalmam sincs mi a fasz van xddd
> HF NÉZD EZT MEG TES!
