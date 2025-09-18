# sql

> standard \[[Relációs algebra]\]-ra alapuló adatbázis kezelő nyelv

______________________________________________________________________

> SELECT -> (π)
>
> > a megadott táblában tetszőleges fügvény is alkalmazható amíg értelmes a végeredmény
> > \* -> Joker szimbólum, bármi jöhet ami stimmel
> > AS -> (ρ)
>
> ______________________________________________________________________
>
> FROM -> ( (*halmaz*) )
>
> > adott halmaz lehet egy másik lekérdezés
>
> ______________________________________________________________________
>
> WHERE -> (σ)
>
> > logikai operátorok (Pl: AND)
> > coparison (kacsacsőr) operátorok
> >
> > > != -> \<>
> > > összetett (kombinált) feltételek
> >
> > ______________________________________________________________________
> >
> > (NOT) LIKE -> mintakeresés stringekben
> >
> > > % -> akármennyi karaktert jelent _ ->
> > > tetszőleges karaktert jelent Oracle-ben felülírhatóak (valahogy xddd)
> > >
> > > felbontható eredményez, de az részletkérdés
> > > nagy/kisbetű fügő:)
> > >
> > > > létezik UPPER(), LOWER() függvény
> >
> > ______________________________________________________________________
> >
> > NULL lehetséges érték
> >
> > > ismeretlen/hiányzó értéket jelelöli átlagosan
> >
> > logika nem bináris hanem trináris
> >
> > > ## TRUE -> 1 UNKNOWN -> 1/2 FLASE -> 0
> > >
> > > így a logikai műveleteket át lehet írni más formába:
> > >
> > > > AND -> MIN
> > > > OR -> MAX
> > > > NOT -> 1-x
> > >
> > > ______________________________________________________________________
> > >
> > > SELECT * FROM tábla WHERE érték > 0 OR érték \<= 0
> > >
> > > > null értéket ignorálja a lekérdezés, és csak azokat a sorokat adja vissza
> > > > ahol van megadva bármi az értéknek
> > > >
> > > > ______________________________________________________________________
> > > >
> > > > IS NOT NULL \<-> érték > 0 OR érték \<= 0 ha kiértékelető mindkettő
> >
> > ______________________________________________________________________
> >
> > IN
> >
> > >

| a | b |
| --- | --- |
| 1 | 2 |
| 3 | 4 |

> > >

| b | c |
| --- | --- |
| 2 | 5 |
| 2 | 5 |

> > > SELECT a FROM R WHERE b IN (SELECT b FROM S); egy soros táblát ad vissza
> > > SELECT a FROM R, S WHERE R.b = S.b; két soros táblát ad vissza
> >
> > ______________________________________________________________________
>
> EXISTS
>
> > > EXISTS() akkor és csak akkor igaz, ha az alkérdés eredménye nem üres.
> >
> > ______________________________________________________________________
> >
> > ANY
> >
> > > x = ANY() akkor és csak akkor igaz, ha x egyenlő az alkérdés legalább egy sorával.
> >
> > ______________________________________________________________________
> >
> > ALL
> >
> > > x \<> ALL() akkor és csak akkor igaz,
> > > ha x az alkérdés egyetlen sorával sem egyezik meg.
>
> ______________________________________________________________________
>
> halmazműveletek értelmezve vannak
>
> > UNION, INTERSECT, MINUS kulcsszavakkal
>
> ______________________________________________________________________
>
> Multihalmaz szemantika (bag semantics) értelmezve van
>
> > motivácó: Hatékonyság
> > Mindenképpen törlődjenek az ismétlődések:
> >
> > > SELECT DISTINCT *(...)*
> >
> > Ne törlődjenek az ismétlődések:
> >
> > > SELECT ALL *(...)*
> > > *(...)* UNION ALL *(...)*
>
> ______________________________________________________________________
>
> Összekapcsolás (join) kifejezések
>
> > Természetes összekapcsolás -> (⨝)
> >
> > > R NATURAL JOIN S
> > > SELECT * FROM tábla1, tábla2 WHERE tábla1.x = tábla2.x
> >
> > ______________________________________________________________________
> >
> > Ön-összekapcsolás (self-join)
> >
> > > SELECT * FROM tábla AS t1, tábla AS t2 WHERE t1.x = t2.x AND *f(t1.y,t2.y)*
> > > f(x,y) => tetszőleges {tuple} -> *L*
> >
> > ______________________________________________________________________
> >
> > Descartes szorzat (azaz Cross Join)
> >
> > > R CROSS JOIN S
> > > SELECT * FROM R , S
> >
> > ______________________________________________________________________
> >
> > Théta-összekapcsolás
> >
> > > R JOIN S ON *\<feltétel>*
