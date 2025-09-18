# logika 7

Prev: \[[Logika 6]\]
Módusz ponens
:\]
whas is das

A, A>B
\- - - -
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

1. A>B [Hip]
1. B>C [Hip]
1. (A>(B>C))>((A>B)>A>C) [A2]
1. (B>C)>(A>(B>C)) [A1,A||B>C,B||A]
1. (A>(B>C)) [mp(2,4)]
1. (A>B)>A>C [mp(3,5)]
1. A>C [mp(1,6)]
   kijön:\]

______________________________________________________________________

{a>(B>C),B} |- A>C

1. A>(B>C) [Hip]
1. B [Hip]
1. (A>(B>C))>((A>B)>A>C) [A2]
1. (A>B)>A>C [mp(1,3)]
1. B>(A>B) [A1,A||B,B||A]
1. A>B [mp(2,5)]
1. A>C [mp(4,6)]
1. késsz:\]\]

______________________________________________________________________

|- !!A > A
-> dedukciós tétel
{!!A} |- A

1. !!A [Hip]
1. (!A>!A)>(!A>!!A)>A
1. (!A>!A) [B1,A||!A]
1. (!A>!!A)>A [mp(2,3)]
1. !!A>(!A>!!A) [A1,A||!!A,B||!A]
1. !A>!!A [mp(1,5)]
1. A [mp(4,6)]
1. kész

______________________________________________________________________

{A>B} |- !!A > !!B
-> dedukciós tétel
{A>B,!!A} |- !!B

1. A>B [Hip]
1. !!A [Hip]
1. !!A>A [B4]
1. A [mp(2,3)]
1. B [mp(1,4)]
1. B > !!B [B3,A||B]
1. !!B [mp(5,6)]
1. kész

______________________________________________________________________

{F>K,K>A,!A} |- !F

1. F>K [Hip]
1. K>A [Hip]
1. !A [Hip]
1. (!!F>!A)>(!!F>!!A)>!F [A3,A||!F,B||!A]
1. !A>(!!F>!A) [A1,A||!A,B||!!F]
1. !!F > !A [mp(3,5)]
1. (!!F>!!A)>!F [mp(4,6)]
1. (F>A)>(!!F>!!A) [B5,A||F,B||A]
1. (F>K)>((K>A)>(F>A)) [B2,A||F,B||K,C||A]
1. (K>A)>(F>A) [mp(1,9)]
1. F>A [mp(2,10)]
1. (!!F>!!A) [mp(8,11)]
1. !F [mp(7,12)]
1. danoníno

______________________________________________________________________

A -> Időben érkezett
B -> Italok az asztalon

1. A>B
1. !B>!A
   {A>B} |- !B>!A
   Dedukciós
   {A>B,!B} |- !A
1. A>B [Hip]
1. !B [Hip]
1. (!!A>!B)>(!!A>!!B)>!A [A3,A||!A,B||!B]
1. !B > (!!A > !B) [A1,A||!B,B||!!A]
1. !!A>!B [mp(2,4)]
1. (!!A>!!B)>!A [mp(3,5)]
1. (A>B)>(!!A>!!B) [B5]
1. (!!A>!!B) [mp(1,7)]
1. !A [mp(6,8)]
1. done

______________________________________________________________________

{!B>!A} |- A>B
-> dedukciós tétel
{!B>!A,A} |- B

1. !B>!A [Hip]
1. A [Hip]
1. (!B>A)>(!B>!!A)>B
1. (!B>!!A)>B [mp(1,3)]
1. A>!!A [B3]
1. !!A [mp(2,5)]
1. !!A>(!B>!!A) [A1,A||!!A,B||!B]
1. !B>!!A [mp(6,7)]
1. B [mp(4,8)]
