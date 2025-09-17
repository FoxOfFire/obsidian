\[[Logika 1]\] volt előző részek tartalmából

> ______________________________________________________________________
>
> - 1 Minden rovar bogár, de nem minden bogár rovar
> - 2 Szarvasnak, a szarvasbogárnak kitines a szárnyfejője
> - 3 Egy rovarnak nincsen kitines szárnyfedője, vagy bogár
> - 4 Szarvas legjobb barátja bogár
>
> ______________________________________________________________________
>
> ## \[[Nullad rend]\]ben
>
> - A ^ !B
> - C
> - D
> - E
>
> ______________________________________________________________________
>
> ## \[[Elsőrend]\]ben
>
> Univerzm: {rovarok}
> Predikátum szimbólumok: (**U**n -> **L**)
>
> - B(x) -> x bogár
> - SZ(x) -> 1 szarvasbogár
> - K(x) -> x-nek kitines a szárnyfedeje
>
> Konstansok:
>
> - *s* -> Szarvas
>
> Függvények:
>
> - lb(x) -> megadaj x legjobb barátját
>
> Interpretációk:
>
> - 1 *A*x(B(x))
> - 2 SZ(*s*) ^ K(*s*)
> - 3 *A*x(!K(x) v B(x))
> - 4 B(lb(*s*))
>
> ______________________________________________________________________
>
> Univerzm: {állatok}
> Predikátum szimbólumok: (**U**n -> **L**)
>
> - B(x) -> x bogár
> - SZ(x) -> 1 szarvasbogár
> - K(x) -> x-nek kitines a szárnyfedeje
> - R(x) -> x rovar
>
> Konstansok:
>
> - *s* -> Szarvas
>
> Függvények:
>
> - lb(x) -> megadaj x legjobb barátját
>
> Interpretációk:
>
> - 1 *A*x(B(x) > R(x))
> - 2 SZ(*s*) ^ K(*s*)
> - 3 *A*x(R(x) > (!K(x) v B(x)))
> - 4 B(lb(*s*))
>
> ______________________________________________________________________
>
> ## Gráf
>
> 0 - 1
> | /
> 2
> | \\
> 3 - 4
>
> U = {0,1,2,3,4}
> Predikátumok:
>
> - E(x,y) -> x és y közt van él
> - =(x,y) -> x és y megegyeznek
>
> Állítások
>
> - 1 *A*x*E*yE(x,y)
> - 2 *E*x*A*yE(x,y) \<- nemjó:(
> - 3 *A*x*A*y(E(x,y) > E(x,y) ^ ! =(x,y))
> - 4 *A*x*E*y*E*z(E(x,y) ^ E(x,z) > E(y,z))
>
> ______________________________________________________________________
>
> Univerzum:
>
> - U = {kutyák} U {emberek}
>
> Predikátum:
>
> - K(x:kutya) -> x kertben él
> - SZ(x:kutya,y:kutya) -> x és y szomszédok
> - G(x:kutya,y:ember) -> x gazdája y
> - H(x:kutya) -> x házban él
>
> Konstansok:
>
> - *z*:kutya -> Zokni
> - *n*:ember -> Norbi
>
> Függvények:
>
> - sz(x:kutya) -> x szomszéja :kutya
> - g(x:kutya) -> x gazdája :ember
>
> Feladatok:
>
> - 1 K(*z*)
> - 2a H(sz(*z*))
> - 2b *E*y(SZ(*z*,y) ^ H(y))
> - 3 G(*z*,*n*)
> - 4 *A*x*E*y( G(x,y) )
> - 5 *E*x*E*y( H(x) ^ K(y) ) \<-- booo (muszáj két külömböző kutyának lenni akkikre igaz az egyik és a másik)
> - 5 *E*x(H(x)) ^ *E*y(K(y))
>
> ______________________________________________________________________
>
> ## Változók előfordulása:
>
> *A*x(P(x) ^ Q(x,y)) > *A*y( Q(z,y) )

| | x | y | z |
| ----- | ------ | ------ | ------ |
| 1 | kötött | szabad | szabad |
| 2 | kötött | kötött | |
| ----- | ------ | ------ | ------ |
| típus | kötött | vegyes | szabad |

> ______________________________________________________________________
>
> ## Prímkomponensek:
>
> *A*x( P(x) ^ Q(x,y) ) > ( *A*yQ(z,y) > (P(a) v Q(w)))
> 1111111111111111111 - 2222222222 - 33333 - 44444
>
> *A*z(P(x) ^ *A*x(Q(x,y) > P(z))) > *A*yQ(z,y) > P(*a*)
> 1111111111111111111111111111 - 22222222 - 3333
>
> mégegy
> nincs kedvem leírni lol
> aza lényeg hogy kvantorokat nem bontjuk fel lol
