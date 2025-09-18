# Logika 1

> ## \[[Logika Követelmények]\] óra
>
> ### \[[Logikai Jelölések]\]
>
> ______________________________________________________________________
>
> ## [Ítéletlogika](https://canvas.elte.hu/courses/47740/files/folder/Gyakorlat) feladatai
>
> ______________________________________________________________________
>
> ## 1
>
> 1 A 2 A > !B 3 (C v B) ^ (!D v C) 4 !(G ^ (!F > D)) 5 (D > E)
> ^ ( E > D) 6 D ^ (G > F) 7 B > (!D v B)
>
> ## Szemantikus tulajdonságok
>
> - \[[kielégíthető]\]
> - \[[kielégíthetetlen]\]
> - \[[tautológia]\]
>
> ______________________________________________________________________
>
> | B | D | !D | !D v B | B > (!D v B) |
> | --- | --- | --- | ------ | ------------ |
> | i | h | i | i | i |
> | h | i | h | h | i |
> | i | i | h | i | i |
> | h | h | i | i | i |
>
> *ez \[[tautológia]\] mivel minden interpretáció kielégíti*
>
> ______________________________________________________________________
>
> (!A > !B) ^ !(A v !B)
>
> | A | B | !A | !B | !A > !B | A v !B | !(A v !B) | (!A > !B) ^ !(A v !B) |
> | --- | --- | --- | --- | ---- | --- | --- | ----------- |
> | i | i | h | h | i | i | h | h |
> | i | h | h | i | i | i | h | h |
> | h | i | i | h | h | h | i | h |
> | h | h | i | i | i | i | h | h |
>
> *ez \[[kielégíthetetlen]\] mivel nincs olyan interpretáció ami kielégíti*
>
> ______________________________________________________________________
>
> \[[Formula halmaz]\]
> F = { A v !B, !(A v B), ...}
> szemantikus következmény
> {F1, F2, ... , Fn} |= G
> {A, A > !B} |= !B

| A | B | A | A > !B | !B | Következmény |
| --- | --- | --- | ------ | --- | --------------- |
| i | i | i | h | h | |
| i | h | i | i | i | itt minden igaz |
| h | i | h | i | h | |
| h | h | h | i | i | |

> a formula halmaz \[[kielégíthető]\]
> {!B, (C v B) ^ (!D v C)} |= C

| B | C | D | !B | (C v B) ^ (!D v C) | C | következmény |
| --- | --- | --- | --- | ------------------ | --- | ------------ |
| i | i | i | h | i | i | |
| i | i | h | h | h | h | |
| i | h | i | h | i | i | |
| i | h | h | h | i | h | |
| h | i | i | i | i | i | minden igaz |
| h | i | h | i | h | h | |
| h | h | i | i | i | i | minden igaz |
| h | h | h | i | h | h | |

> *a formula halmaz \[[kielégíthető]\] mivel van igaz interpretáció*
>
> ______________________________________________________________________
>
> *zsárójel elhagyós feladat xd nincs kedvem kiírni*
>
> ______________________________________________________________________

| A | B | B > A | A v B | A v !A | következméyn |
| --- | --- | ----- | ----- | ------ | ------------ |
| i | i | i | i | i | igaz |
| i | h | i | i | i | igaz |
| h | i | h | i | i | |
| h | h | i | h | i | |

> A v !A 0ad fokon tautológia
