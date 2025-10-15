# Számelm Gyak 6

## Predikátum logika

### Nyelv részei

> **Indivídum:** X1,Y ...
> **Predikátum:** P,Q ...
> **Function:** f,g ...
> **Constans:** a,b ...
>
> mindnek van aritása (a konstansnak mindig 0)
>
> **Termek**
> X€Ind -> X€Term
> a€Cnst -> a€Term
>
> **Formulák**
> P€Pred,t1...tar€Term -> P(t1..tar)€Form|
> F€Form -> ¬F€Form
> F,K€Form -> FoK€Form o€{^,v}
> F€Form -> AxF, ExF €Form

## Ex

> f(2),g(1)€Func, a€Cnst, P(2),Q(1)€Pred
>
> f(f(x,y),a)
> f(x,y,x)
> g(x,f(x,y))
> Axq(x)
> P(x,y)^¬q(z)
> p(x,y)
> Azq(x)
> p(x,p(y,z))

## Szerkezeti fák

> ¬( Ax p(x,y) > Ex r(z) v r(y))
> *fa rajz lol xd*
>
> Atomi formula: p(t1...tar)
> Prím formula: Axp(t1...tar)
>
> az a prím részformula prímkomponens ami nem részformulája semmilyen prím formulája
>
> príkomponensek visszavezethetőek 0adrendre és annak az igazságtábláját hívjuk Quine-táblának

## Szemantika

> I = \<U,Ipred,Ifunc,Iconst>
> U -> Alaphalmaz
> Ipred -> relációk
> Ifunc -> műveletek
> Iconst -> €U
>
> U := {A,B}
> Axq(x) -> tfh hamis
> de ha U := {J,K}
> akkor már lehet Axq(x) igaz

### Ex2

> **I**
> U = N
> p(x,y) -> y=x^2
> q(x) -> x prím szám
> f(x,y) -> x+y
> g(x) -> x+1
> a := 0
>
> **K:**
> x -> 7
> y -> 11
> z -> 2
>
> |f(g(a),y)| -> 12
> |p(g(z),f(x,z))| -> igaz
> |¬q(y)>q(z)| -> igaz
> |Ax(p(x,y)>q(z))| -> igaz
> |Ex(p(x,y))| -> hamis
> |AxEy(p(x,y))| -> igaz
>
> Ax(p(x,y) v q(x)) > AzEx(p(x,z)) v q(z)
> x -> kötött
> z -> vegyes
> y -> szabad
> formula zárt ha csak kötött indivídum változó van benne
> formula nyitott ha van benne szabad indivídum változó előfordulás
>
> y,z -> paraméter
> értéktábla kiértékelése problémás p€N paraméterre is már

### Ex3

> U = {0,1,2}
> p -> p', q -> q'
> f(x,y) -> (x+y)%3
> a -> 0, b -> 1
> p' = {(0,1),(0,2),(2,1),(2,2)}
> q' = {(0),(2)}
>
> Ax(p(x,y)) v q(y)
>
> |y|Ax(x,y)|q(x)|Ax(p(x,y)) v q(y)|
> |---|---|---|---|
> |0|h|i|i|
> |1|h|h|h|
> |2|h|i|i|
>
> |= F -> logikai törvény
> |=0 F -> Tautológiusan igaz
> (|=0 F) -> (|= F)
