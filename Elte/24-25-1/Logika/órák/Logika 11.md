szekvent gyak

P(x),R(x) -> *E*xP(x),P(x) (azon)); P(x),R(x) -> *E*xR(x),R(x) (azon)
P(x),R(x) -> *E*xP(x) (->*E*); P(x),R(x) -> *E*xR(x) (->*E*)
P(x)^R(x) -> *E*xP(x) (^->); P(x)^R(x) -> *E*xR(x) (^->)
*E*x(P(x)^R(x)) -> *E*xP(x) (*E*->); *E*x(P(x)^R(x)) -> *E*xR(x) (*E*->)
*E*x(P(x)^R(x)) -> *E*xP(x) ^ *E*xR(x) (->^)

______________________________________________________________________

# rezolúció:

Kielégíthetetlenség vizsgálat mindig
szintaktikus kalkulus

knf -> konyukciós normálforma
rezolúció: knf->diszjunkció halmaz

Először:

> A>B => !AvB

Másodiknak:

> !!A => A
> !(AvB) => !A^!B
> !(A^B) => !Av!B

Utoljára

> A^(BvC) => (A^B)v(A^C)
> Av(B^C) => (AvB)^(AvC)

______________________________________________________________________

Klózhalmaz alkotás
{(Y>!(!X^!Z))^(XvY), !(X^!Z), !Z}

{(Y>!(!X^!Z))^(XvY), !Xv!!Z, !Z}
{(Y>!(!X^!Z))^(XvY), !XvZ, !Z}
{(!Yv!(!X^!Z))^(XvY), !XvZ, !Z}
{(!Yv!!Xv!!Z)^(XvY), !XvZ, !Z}
{(!Yv!!XvZ)^(XvY), !XvZ, !Z}
{(!YvXvZ)^(XvY), !XvZ, !Z}
{!YvXvZ, XvY, !XvZ, !Z}

1. !YvXvZ [eS]
1. XvY [eS]
1. !XvZ [eS]
1. !Z [eS]
1. YvZ [res(2,4)]
1. f ZvX [res(1,5)]
1. f X [res(4,6)]
1. Z [res(3,7)]
1. [] [res(3,8)]

S = {!FvK, !KvA, !A, F}

1. !FvK [eS]
1. !KvA [eS]
1. !A [eS]
1. F [eS]
1. K [res(1,4)]
1. A [res(2,5)]
1. [] [res(3,6)]

______________________________________________________________________

{(AvB)>C} |- (A>C)^(B>C)
kielégíthetetlenségehet következmény negáltját be a halmazba
(AvB)>C, !((A>C)^(B>C)) => implikációk kezelése
!(AvB)vC, !((!AvC)^(!BvC)) => negációk
(!A^!B)vC, !(!AvC)v!(!BvC) => negációk
(!A^!B)vC, (!!A^!C)v(!!B^!C) => negációk
(!A^!B)vC, (A^!C)v(B^!C) => azonosságok
(!AvC)^(!BvC), (AvB)^!C => knf -> klózhalmaz
S ={!AvC,!BvC,AvB,!C}

> egység rezolúció

1. !AvC [eS]
1. !BvC [eS]
1. AvB [eS]
1. !C [eS]
1. !A [res(1,4)]
1. !B [res(2,4)]
1. A [res(3,5)]
1. [] [res(5,7)]

> lineáris input rezolúció

1. !AvC [eS]
1. !C [eS]
1. !A [res(1,2)]
1. AvB [eS]
1. B [res(3,4)]
1. !BvC [eS]
1. C [res(5,6)]
1. !C [eS]
1. [] [res(7,8)]

______________________________________________________________________

szemantikus fa?
XvY^!Z
bázis: X,Y,Z
őő
rajzolni kell
xd
