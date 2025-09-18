# logika 8

Prev : ZH and \[[Logika 7]\]

> ítélet kalkulus
> {!Y^(!!X>!Z),!Z>!(Xv!Y)}|- Z
>
> 1. !Y^(!!X>!Z) [Hip]
> 1. !Z>!(Xv!Y) [Hip]
> 1. (!Z>Xv!Y)>(!Z>!Xv!Y)>Z [A3,A||Z21,B||Xv!Y]
> 1. !Y^(!!X>!Z)>!Y [C1,A||!Y,B||!!X>!Z]
> 1. !Y [mp(1,4)]
> 1. !Y>Xv!Y [D1,A||X,B||!Y]
> 1. Xv!Y [mp(5,6)]
> 1. (Xv!Y)>!Z>(Xv!Y) [A1,A||Xv!Y,B||!Z]
> 1. !Z>(Xv!Y) [mp(7,8)]
> 1. (!Z>!Xv!Y)>Z [mp(3,9)]
> 1. Z [mp(2,10)]

______________________________________________________________________

Természetes levezetés:
A|-A
|-A>A (>b)

______________________________________________________________________

A,!A|-A , A,!A|-!A
A|-!!A (!B)
|-A>!!A (>b)

______________________________________________________________________

!!A|-!!A (!a)
!!A|-A (>b)
|-!!A>A

______________________________________________________________________

{A>B,B>c}|-A>C

A>B,B>C,A,!C|-A (azon) , A>B,B>C,A,!C|-A>B (azon)\
A>B,B>C,A,!C|-B (>a) , A>B,B>C,A,!C|-B>C (azon)
A>B,B>C,A,!C|-C (>a) , A>B,B>C,A,!C|-!C (azon)
A>B,B>C,A|-!!C (!b)
A>B,B>C,A|-C (!a)
A>B,B>C|-A>C (>b)
(itt nem kellett volna a negációt bevezetni, de az részletkérdés)

______________________________________________________________________

{AvB > C} |- (A>C) v (B>C)

AvB>C,B|-B (azon)
AvB>C,B|-AvB (vb) , AvB>C,B|-AvB>C (azon)
AvB>C,B|-C (>a)
AvB>C|-B>C (>b)
AvB>C|-(A>C)v(B>C) (vb)

______________________________________________________________________

|- A>(!A>B)

A,!A,!B|-!A (azon) , A,!A,!B|- A (azon)
A,!A|-!!B (!b)
A,!A|-B (!a)
A|-!A>B (>b)
|- A>(!A>B) (>b)

______________________________________________________________________

{F>K,K>A,!A}|-!F

F>K,K>A,!A,F|-F (azon) , F>K,K>A,!A,F|-F>K (azon)
F>K,K>A,!A,F|-K (>a) , F>K,K>A,!A,F|-K>A (azon)
F>K,K>A,!A,F|-A (>a) , F>K,K>A,!A,F|-!A (azon)
F>K,K>A,!A|-!F (!b)

______________________________________________________________________

!(A^(B>C))>(A>C)

!(A^(B>!C)),A,!C,B|-!C (azon)
!(A^(B>!C)),A,!C|-B>!C (>b) , !(A^(B>!C)),A,!C|-A (azon)
!(A^(B>!C)),A,!C|-A^(B>!C) (^b), !(A^(B>!C)),A,!C|-!(A^(B>!C)) (azon)
!(A^(B>!C)),A|-!!C (!b)
!(A^(B>!C)),A|-C (!a)
!(A^(B>!C))|-A>C (>b)
|-!(A^(B>!C))>(A>C) (>b)

______________________________________________________________________

(A>C)>((B>C)>(AvB>C))
A>C,B>C,A|-A (azon) , A>C,B>C,A|-A>C (azon) ,A>C,B>C,B|-B>C (azon) ,
    A>C,B>C,B|-B (azon)\
A>C,B>C,A|-C (>a), A>C,B>C,B|-C (>a)
A>C,B>C,AvB|-C (va)
A>C,B>C|-AvB>C (>b)
(A>C)|-((B>C)>(AvB>C)) (>b)
|-(A>C)>((B>C)>(AvB>C)) (>b)
