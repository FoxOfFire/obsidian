[[NM1_ea00.pdf]]
[[NM1_ea01.pdf]] p(27-ig)
## Furca jelenségek
Összeadás nem asszociatív
a = 1e-20 ; b = 1
(a+b)-b = 0 ; a+(b-b) = a
Integrállal bemutatott példán át szemléltettük hogy algoritmikus instabilitás milyen problémát tud okozni a kiszámításban
Numerikus stabilitás fontosságát kiemelte
## Gépi számok lebegőpontos modellje
0.1MANTISSZA\*2^KARAKTERISZTIKA
jelőlés:
- M(3,-1,2) +-0.1__\*2^k (-1<=k<=2)
- ε0 = \[100...0|k−] = 1 2 · 2^(k-) = 2^(k- - 1)
- ε1 = \[100...01|1] − \[100...00|1] = 2^−t · 2^1 = 2^(1−t)
- M∞ = \[111...11|k+] = 1.00...00\*2k+ − 0.00...01\*2k+ = (1−2^−t)\*2^k+

float ∼ M(23, −128, 127), double ∼ M(52, −1024, 1023)

Két létező lebegő pontos szám közé kell belőni az ábrázoláshoz a pontos értéket, aminek kerekítéséhez (ε1)/2-vel arányos hibát kell lefogadnunk kerekítésnél.

## Hibaszámítás
- Đ a := A-a a közelítő érték (pontos) hibája
- |Đ a| := |A-a| a közelítő érték abszolít értéke
- (Đa) >= |Đ a| az a egy abszolút hibakorlátja
- d a := Đ a / A ≈ Đ a / a az a relatív hibája
- (da) >= |d a|
Műveleti hibák
- relatív hibakorlát magas ha két közeli számot vonunk ki egymásból
- abszolút hibakorlát magas ha relatíve nagy számot osztunk relatíve kicsi számmal
- (Hibaszámítást bizonyítottuk összeadásra)
