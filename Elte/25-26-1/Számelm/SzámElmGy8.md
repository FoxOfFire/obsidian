# gy8

## új számítás modell

### prevously

- végesautómták (reguláris nyelvek)
- veremautómaták (2es típusú nyelvek)

### now: turing gép

mindenre képes ami kiszámítható algoritmikusan

író/olvasó feje van
jobbra/ballra mozogHAT

üres szalagrész létezik és jelölése _

M=<Q,S,G,d,q0,qi,qn>
Q -> Állapotok halmaza
S (Szigma) -> input
G (gamma) -> szalag szinbólumhalmaza (S€G)
d (delta) -> (Q\{qi,qn})xG->QxGx{R,L,S}
q0 -> kezdő állapot
qi -> elfogadó állapot (terminál ebbe érkezéssel)
qn -> elutasító állapot (terminál ebbe érkezéssel)

nincs olyan hogy nem definiált átmenet, mindent definiálunk

b/c,R -> b-t olvasunk kicseréljük c-re és jobbralépünk

uqv -> u,v€G* | v!=e

> ab(q1)ba -> abba és a második b-n van az olvasófej
ezáltal alkalmazva a b/c,R -t
> abc(q2)a
a/a,R
> abca(q3)_

kezdökonfig:
> q0U | U€S

megállási konfig:
>u(qi)v vagy u(qn)v

## feladat

### 1 tg ami 7-el osztható hosszúságú szavakat ismeri fel

állapotok:

- q0 -> szóhossz % 7 = 0
- q1 -> szóhossz % 7 = 0
- q2 -> szóhossz % 7 = 0
- q3 -> szóhossz % 7 = 0
- q4 -> szóhossz % 7 = 0
- q5 -> szóhossz % 7 = 0
- q6 -> szóhossz % 7 = 0

szabálytípusok:

- q(n): t/_,R ->q((n+1)%7) (n€{0,1..6})
- q0: _/_,R -> qi
- q(n): _/_,R -> qn (n€{1,2..6})
- (A más => qn)

művelet igény: O(n)

### 2 L(M) = {w€{a,b}*|w=w^-1}

q0:
>a/_,R -> q1
>b/_,R -> q2
>_/_,S -> qi

q1:
>a/a,R -> q1
>b/b,R -> q1
>_/_,L -> q3

q2:
>a/a,R -> q2
>b/b,R -> q2
>_/_,L -> q4

q3:
>a/_,L -> q5
>b/_,S -> qn
>_/_,S -> qi

q4:
>a/_,S -> qn
>b/_,L -> q5
>_/_,S -> qi

q5:
>a/a,L -> q5
>b/b,L -> q5
>_/_,R -> q0

0abba levezetése:
> 0abba
> 1bba
> b1ba
> bb1a
> bba1_
> bb3a
> b5b
> 5bb
> 5_bb
> 0bb
> 2b
> b2_
> 4b
> 5_
> 0_
> i_

művelet igény: O(n^2)
