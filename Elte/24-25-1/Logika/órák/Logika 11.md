szekvent gyak

P(x),R(x) -> *E*xP(x),P(x) (azon)); P(x),R(x) -> *E*xR(x),R(x) (azon)
P(x),R(x) -> *E*xP(x) (->*E*); P(x),R(x) -> *E*xR(x) (->*E*)
P(x)^R(x) -> *E*xP(x) (^->); P(x)^R(x) -> *E*xR(x) (^->)
*E*x(P(x)^R(x)) -> *E*xP(x) (*E*->); *E*x(P(x)^R(x)) -> *E*xR(x) (*E*->)
*E*x(P(x)^R(x)) -> *E*xP(x) ^ *E*xR(x) (->^)

---
# rezolúció:
Kielégíthetetlenség vizsgálat mindig
szintaktikus kalkulus

knf -> konyukciós normálforma
rezolúció: knf->diszjunkció halmaz

Először:
>A>B => !AvB

Másodiknak:
>!!A => A
>!(AvB) => !A^!B
>!(A^B) => !Av!B

Utoljára
>A^(BvC) => (A^B)v(A^C)
>Av(B^C) => (AvB)^(AvC)

---
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
2. XvY [eS]
3. !XvZ [eS]
4. !Z [eS]
5. YvZ [res(2,4)]
6. f ZvX [res(1,5)]
7. f X [res(4,6)]
8. Z [res(3,7)]
9. [] \[res(3,8)]

S = {!FvK, !KvA, !A, F}
1. !FvK [eS]
2. !KvA [eS]
3. !A [eS]
4. F [eS]
5. K [res(1,4)]
6. A [res(2,5)]
7. [] \[res(3,6)]
---
{(AvB)>C} |- (A>C)^(B>C)
kielégíthetetlenségehet következmény negáltját be a halmazba
(AvB)>C, !((A>C)^(B>C)) => implikációk kezelése
!(AvB)vC, !((!AvC)^(!BvC)) => negációk
(!A^!B)vC, !(!AvC)v!(!BvC) => negációk
(!A^!B)vC, (!!A^!C)v(!!B^!C) => negációk
(!A^!B)vC, (A^!C)v(B^!C) => azonosságok
(!AvC)^(!BvC), (AvB)^!C => knf -> klózhalmaz
S ={!AvC,!BvC,AvB,!C}
>egység rezolúció
1. !AvC [eS]
2. !BvC [eS]
3. AvB [eS]
4. !C [eS]
5. !A [res(1,4)]
6. !B [res(2,4)]
7. A [res(3,5)]
8. [] \[res(5,7)]
> lineáris input rezolúció
1. !AvC [eS]
2. !C  [eS]
3. !A [res(1,2)]
4. AvB [eS]
5. B [res(3,4)]
6. !BvC [eS]
7. C [res(5,6)]
8. !C  [eS]
9. [] \[res(7,8)]

---
szemantikus fa?
XvY^!Z
bázis: X,Y,Z
őő 
rajzolni kell
xd






