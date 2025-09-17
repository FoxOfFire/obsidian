# paralelizáció

> "*kevés idő sok anyaghoz*"
> java
> *nézd át lol*
> hatékonyabb
> több ügyfélnél releváns
>
> ## kommunikáció
>
> > osztott memória több processzor felett
> > logikailag több szálra tagolt kód közti kommunikáció
> > interprocesszor kommunikáció
>
> ## Kevesesbb processzor mint folyamat
>
> > procik felváltva futtatják a processzeket
> > látszólagos párhuzamosság
> > blokkolt folyamat nem problémás
> > váltás overhead-el rendelkezik
>
> nem processzek közti kommunikációval dolgozunk, hanem szálakkal
> (alacsonyabb váltási overhead költség)
>
> ## Java specific
>
> > beépívett támogatással rendelkezik
> > *liba*
>
> ## Nehézségek
>
> > nem deretmenisztikusság
> > nehezen átlátható
> > kezelendő:
>
> - ütemezés
> - interferencia
> - szinkronizáció
> - kommunikáció
>
> ## Szálak létrehozása
>
> > implicit szállétrehozás (főszál, garbage-collector, gui)
> > Thread oszály példányosított objektumon keresztül indítjuk az új szálat
> > *(new Thread()).start();*
> > extendelni kell a Thread osztályt és úgy lehet értelmes threadet alkotni
> > akkor fejeződik be a program ha a nem daemon szálak befejeződnek
> > a *start()* metódus felel azért hogy a szál ténylegesen elinduljon
> > a *run()* metódust kell felüldefiniálni, az a szál tényleges logikai funkciója
>
> a szálak közötti erőforráskiosztás nem determinisztikus
