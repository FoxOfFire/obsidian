Prev: [[Logika 6]]
Módusz ponens
:]
whas is das

A, A>B
\- \- \- \-
B
fentiből következik a lenti

was ist helyesség és teljesség?akkor 
helyesség 
- ha |-, akkor |=
teljes:
- ha |=, akkor |-

itélet kalkulus helyes és teljes
szemantikus kövezkezmény -> |=
szintaktikus kövektezmény -> |-

{A>B,B>C} |- A>B
1. A>B \[Hip]
2. B>C \[Hip]
3. (A>(B>C))>((A>B)>A>C) \[A2]
4. (B>C)>(A>(B>C)) \[A1,A||B>C,B||A]
5. (A>(B>C)) \[mp(2,4)]
6. (A>B)>A>C \[mp(3,5)]
7. A>C \[mp(1,6)]
kijön:]
---

{a>(B>C),B} |- A>C
1. A>(B>C) \[Hip]
2. B \[Hip]
3. (A>(B>C))>((A>B)>A>C) \[A2]
4. (A>B)>A>C \[mp(1,3)]
5. B>(A>B) \[A1,A||B,B||A]
6. A>B \[mp(2,5)]
7. A>C \[mp(4,6)]
8. késsz:]]

---
|- !!A > A
-> dedukciós tétel
{!!A} |- A
1. !!A \[Hip]
2. (!A>!A)>(!A>!!A)>A
3. (!A>!A) \[B1,A||!A]
4. (!A>!!A)>A \[mp(2,3)]
5. !!A>(!A>!!A) \[A1,A||!!A,B||!A]
6. !A>!!A \[mp(1,5)]
7. A \[mp(4,6)]
8. kész

---

{A>B} |- !!A > !!B
-> dedukciós tétel
{A>B,!!A} |- !!B
1.  A>B \[Hip]
2. !!A \[Hip]
3. !!A>A \[B4]
4. A \[mp(2,3)]
5. B \[mp(1,4)]
6. B > !!B \[B3,A||B]
7. !!B \[mp(5,6)]
8. kész

---

{F>K,K>A,!A} |- !F
1. F>K \[Hip]
2. K>A \[Hip]
3. !A \[Hip]
4. (!!F>!A)>(!!F>!!A)>!F \[A3,A||!F,B||!A]
5. !A>(!!F>!A)  \[A1,A||!A,B||!!F]
6. !!F > !A \[mp(3,5)]
7. (!!F>!!A)>!F \[mp(4,6)]
8. (F>A)>(!!F>!!A) \[B5,A||F,B||A]
9. (F>K)>((K>A)>(F>A)) \[B2,A||F,B||K,C||A]
10. (K>A)>(F>A) \[mp(1,9)]
11.  F>A \[mp(2,10)]
12. (!!F>!!A) \[mp(8,11)]
13. !F \[mp(7,12)]
14. danoníno
---

A -> Időben érkezett
B -> Italok az asztalon

1. A>B
2. !B>!A
{A>B} |- !B>!A
Dedukciós
{A>B,!B} |- !A
1. A>B \[Hip]
2. !B \[Hip]
3. (!!A>!B)>(!!A>!!B)>!A \[A3,A||!A,B||!B]
4. !B > (!!A > !B) \[A1,A||!B,B||!!A]
5. !!A>!B \[mp(2,4)]
6. (!!A>!!B)>!A \[mp(3,5)]
7. (A>B)>(!!A>!!B) \[B5]
8. (!!A>!!B) \[mp(1,7)]
9. !A \[mp(6,8)]
10. done
---


{!B>!A} |- A>B
-> dedukciós tétel
{!B>!A,A} |- B
1. !B>!A \[Hip]
2. A \[Hip]
3. (!B>A)>(!B>!!A)>B
4. (!B>!!A)>B \[mp(1,3)]
5. A>!!A \[B3]
6. !!A \[mp(2,5)]
7. !!A>(!B>!!A) \[A1,A||!!A,B||!B]
8. !B>!!A \[mp(6,7)]
9. B \[mp(4,8)]







