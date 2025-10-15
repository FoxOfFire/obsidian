# Számítás elmélet gyak 5

## Ítélet tábla

> Két logikai formula logikailag eqvivalens ha ítélet táblája megeggyezik
> lehet logikai formulák közt következményt is vizsgálni
> lehet formulahalmazból is megtenni ezt

## feladat 1

> A: x>(y>X) -> |=A (A tautológia)
> ¬Xv(¬YvX) ~ ¬YvT ~ T

## feladat 2

> ¬(Xv(Y^(Z>X))) ~ ¬X^(Y>Z)
> ¬X^¬(Y^(Z>X))
> ¬X^(¬Yv¬(Z>X))
> ¬X^(¬Yv¬(¬ZvX))
> ¬X^(¬Yv(Z^¬X))
> ¬X^((¬YvZ)^(¬Yv¬X))
> ¬X^(¬YvZ)^(¬Yv¬X)
> ¬X^(¬YvZ)
> ¬X^(Y>Z)

## fogalmak

> literál A vagy ¬A
> elemi konyukció -> Y^(Z^¬X), Z, Z^¬X, ...
> elemi diszjunkció -> Yv(Zv¬X), Z, Zv¬X, ... (AKA klóz)
> DNF -> (Z^¬X)v(Y^X^¬Y)vZ
> KNF -> (Zv¬X)^(YvXv¬Y)^Z
> KDNF -> (Z^¬X^Y)v(Y^X^¬Z)v(Z^X^Y)
> KKNF -> (Zv¬XvY)^(YvXv¬Z)^(ZvXvY)

## minek felel meg az alábbi kifejezés

> X>Y -> semmi:)
> ¬Z -> elemi konyukció/diszjunkció, KNF,DNF
> X^¬Y^Z -> elemi konyukció, DNF, KNF, KDNF
> (Xv¬Y)^Y -> KNF
> (X^Y^¬Z)v(¬X^Y^Z) -> DNF, KDNF

## tétel

> minden ítéletlogikai formulához adható KND és DNF is

## bemutatás

> (X>Y)>¬(X^Y)
> ¬(¬XvY)v¬(X^Y)
> (X^¬Y)v¬Xv¬Y -> DNF
> (Xv¬Xv¬Y)^(¬Yv¬Xv¬Y) -> KNF

## módszeresen

> |X|Y|(X>Y)^¬Y|
> |---|---|---|
> |i|i|h|
> |i|h|h|
> |h|i|h|
> |h|h|i|
>
> **DNF**
> (¬X^¬Y) v ...
>
> **KNF**
> (¬Xv¬y)^(¬XvY)^(Xv¬Y)
>
> {A,B,C} |= D
> igaz ha {A,B,C,¬D} kielégíthetetlen

## Rezolúció

> S: {A1,A2,...}
>
> - A € S
> - res(2 előző eleme a sorozatnak)
>   res(Xv¬Y,¬XvZ) = ¬YvZ
>
> S={¬XvY,X,¬Y}
>
> 1. X € S
> 1. ¬XvY € S
> 1. Y res(1,2)
> 1. ¬Y € S
> 1. [] res(3,4)

## komplex feladat

> A1: Ha elmegyünk P-re, H-re is K-re is
> A2: Ha nem megyünk K-re akkor H-re is
> A3: Ha elmegyünk K-re akkor P-re is
>
> Biz: Elmegyünk H-re
>
> ítélet változók: P K H
> A1: P>H^K ~ (¬PvH)^(¬PvK)
> A2: ¬K>H ~ KvH
> A3: K>P ~ ¬KvP
> ¬B: ¬H
>
> S:{¬PvH,¬PvK,KvH,¬KvP,¬H}
>
> 1. ¬H €S
> 1. ¬PvH €S
> 1. ¬PvK €S
> 1. KvH €S (Kihagyható)
> 1. ¬KvP €S
> 1. ¬P res(1,2)
> 1. K res(3,6)
> 1. P res(5,7)
> 1. [] res(6,8)

## komplex feladat 2

> A1: Minden ember halandó -> A
> A2: Szokrátész ember -> A
> B: Szokrátész halandó -> A
