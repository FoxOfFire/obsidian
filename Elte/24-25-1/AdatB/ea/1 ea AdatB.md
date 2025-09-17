\[[AdatB Követelmények]\]
\[[otthoni ssh setup]\]

> ## mi az \[[adatbázis]\]
>
> példa:
>
> - oktatók: *id, név, beosztás*
> - tárgyak: *név, oktató id, bevezetés éve*
> - teremhasználat: *épület, szobaszám, időköz, tárgynév*
> - egyszerre egy tárgy lehet egy szobában
>
> ______________________________________________________________________
>
> ötlet nyers fájlok
>
> - boo dogdoodoo mert mert külön kódot kellene írni rá
> - ez a doodoo kód minden létező problémára kéne hogy figyeljen mindig és az nem éppen előnyös
>
> ______________________________________________________________________
>
> problémák:
>
> - kéne hozzá egy olyan API is amivel más emberke is eltudná érni az adatokat
> - paralelizációs problémák
> - mivan ha behal a rendszer és elveszik parancs
> - szándékosan duplikált bázisok közti szinkronizáció
>
> ______________________________________________________________________
>
> History
>
> - kőtáblák -> papiusz tekercse -> kartoték rendszerek -> könyvtárak
> - kezdeti adattároló rendszerek
> - alkalmazás: sok kis adathoz sok emberfér hozzá és sokat módosítanak ie: banki rendszerek
> - implementáció: hierarchikus és hálós adatrendszerek *(nem támogattak magas szintü lekérdező nyelvet)*
> - 70s: relációs adatmodellek kitalálva Ted Codd által
> - 90s: elterjed ez a nyelvforma
> - \[[SQL]\]*(Structured Query Language)* magas szintű lekérdezéseket tett lehetővé
> - now: komplexebb adatok *(pl képek videók)* is lekérdezhetőek már
> - hatalmas *(petabájtos)* rendszerek is vannak már
> - adatbázisok adatbázisa ilyen összefogó rendszereken keresztül is van
>
> ______________________________________________________________________
>
> ## Relációs \[[adatmodell]\]
>
> - táblákban tároljuk el az adatokat
> - atribútumokat tárolunk (az első sor xd, oszlopok nevei magyarul)
> - reláció atribútumok halmaza -> relációsémát tárolunk
> - egy-egy reláció soroknak egy halmaza
> - tábla adatok váltók
> - relációk itt matematikailag vannak értelmezve (Descartes-szorzat)
> - sorrend nem számít elvileg, gyakorlatilag muszáj valahogy kiírnunk az adatokat lol
> - táblában tárolt adatok *(elvileg)* atomi *(attól függően hogy mit tartunk atominak)*
> - tárolunk néha kulcsot ami sorok közt egyedi
>
> ______________________________________________________________________
>
> ## \[[Relációs algebra]\]

Next on \[[2 ea AdatB]\]
