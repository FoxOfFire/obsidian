Prev : ZH and [[Logika 7]]
>ítélet kalkulus
>{!Y^(!!X>!Z),!Z>!(Xv!Y)}|- Z
>1. !Y^(!!X>!Z) \[Hip]
>2. !Z>!(Xv!Y) \[Hip]
>3. (!Z>Xv!Y)>(!Z>!Xv!Y)>Z \[A3,A||Z21,B||Xv!Y]
>4. !Y^(!!X>!Z)>!Y \[C1,A||!Y,B||!!X>!Z]
>5. !Y \[mp(1,4)]
>6. !Y>Xv!Y \[D1,A||X,B||!Y]
>7. Xv!Y \[mp(5,6)]
>8. (Xv!Y)>!Z>(Xv!Y) \[A1,A||Xv!Y,B||!Z]
>9. !Z>(Xv!Y) \[mp(7,8)]
>10. (!Z>!Xv!Y)>Z \[mp(3,9)]
>11. Z \[mp(2,10)]

----
Természetes levezetés:
A|-A
|-A>A (>b)

---
A,!A|-A , A,!A|-!A
A|-!!A (!B)
|-A>!!A (>b)

---
!!A|-!!A (!a)
!!A|-A (>b)
|-!!A>A

---
{A>B,B>c}|-A>C

A>B,B>C,A,!C|-A (azon) , A>B,B>C,A,!C|-A>B (azon)  
A>B,B>C,A,!C|-B (>a) ,  A>B,B>C,A,!C|-B>C (azon)
A>B,B>C,A,!C|-C (>a) , A>B,B>C,A,!C|-!C (azon)
A>B,B>C,A|-!!C (!b)
A>B,B>C,A|-C (!a)
A>B,B>C|-A>C (>b)
(itt nem kellett volna a negációt bevezetni, de az részletkérdés)

----
{AvB > C} |- (A>C) v (B>C)

AvB>C,B|-B (azon)
AvB>C,B|-AvB (vb) , AvB>C,B|-AvB>C (azon)
AvB>C,B|-C (>a)
AvB>C|-B>C (>b)
AvB>C|-(A>C)v(B>C) (vb)

---
|- A>(!A>B)

A,!A,!B|-!A (azon) , A,!A,!B|- A (azon)
A,!A|-!!B (!b)
A,!A|-B (!a)
A|-!A>B (>b)
|- A>(!A>B) (>b)

---
{F>K,K>A,!A}|-!F

F>K,K>A,!A,F|-F (azon) , F>K,K>A,!A,F|-F>K (azon) 
F>K,K>A,!A,F|-K (>a) , F>K,K>A,!A,F|-K>A (azon)
F>K,K>A,!A,F|-A (>a) , F>K,K>A,!A,F|-!A (azon) 
F>K,K>A,!A|-!F (!b)

---
!(A^(B>C))>(A>C)

!(A^(B>!C)),A,!C,B|-!C (azon)
!(A^(B>!C)),A,!C|-B>!C (>b) , !(A^(B>!C)),A,!C|-A (azon)
!(A^(B>!C)),A,!C|-A^(B>!C) (^b), !(A^(B>!C)),A,!C|-!(A^(B>!C)) (azon)
!(A^(B>!C)),A|-!!C (!b)
!(A^(B>!C)),A|-C (!a)
!(A^(B>!C))|-A>C (>b)
|-!(A^(B>!C))>(A>C) (>b)

---

(A>C)>((B>C)>(AvB>C))
A>C,B>C,A|-A (azon) , A>C,B>C,A|-A>C (azon) ,A>C,B>C,B|-B>C (azon) , A>C,B>C,B|-B (azon)  
A>C,B>C,A|-C (>a), A>C,B>C,B|-C (>a)
A>C,B>C,AvB|-C (va)
A>C,B>C|-AvB>C (>b)
(A>C)|-((B>C)>(AvB>C)) (>b)
|-(A>C)>((B>C)>(AvB>C)) (>b)