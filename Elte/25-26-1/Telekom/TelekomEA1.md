# Részlegges *(mert késtem lol)*

> Router típusok Pl:
> Vezeték típusok Pl:
>
> > optikai
> > rézvezeték
> > vezetéknélküli
>
> ## Internet = hálózatok hálóztat
>
> > lokális hálózatokat összekötő metahálózat
>
> ## régen telefonos hálózaton keresztül történt
>
> > Digital subscribe Line (DSL)
> > korábbi infrastruktúra újrahasznosítva
> > 3 csatorn (le, fel telefon)
>
> ## Kábeltévé hálózaton keresztül
>
> > Cable Access Technology (CATV)
> > hasonló jellemzők a DSL-hez
> > problémás volt hogy bizonyos háztartások osztoztak a koax
> > sávszélességen, így variabilis volt a sebessége
>
> ## Ethernet leggyakrabban használt LAN tech (Local Area Network)
>
> > akár gigabites sebességet is el tud érni
> > akár optikai kábel is elérhető nem csak sodortt kábelpáros
>
> ## Belső elrendezése
>
> > *bazinagy* gráf
> > 3 fontos tulajdonsága:
> >
> > Hibatolerancia (kikerülhető csúcsok a gráfban)
> > Rugalmasság (extra linkek (csomópontok) nem diszruptívak)
> > Megfelelő csomópont-kapacitás (Linkek száma kellően magas)
> >
> > ### Topológia típusok
> >
> > Teljesen összekötött (jól a hibatűrése, de kihasználatlan)
> > Lánc/gyűrű (könnyen kialakulhatnak hotspotok, és rossz a hibatoleranciája)
> > Bus (*"arról ne is beszéljünk :/"*)
> > Switch-elt hálók (rugalmas és fasza, de okosnak kell lennie a switcheknek)
>
> ## Linkerek és Switchek
>
> > Erőforrás kezelés a bizonyos adatfolyamok között fontos probléma
> >
> > ### Előre lefoglalt
> >
> > > Előre le kell foglalni az igényed és vissza is kell azt adni
> > > Folyamszintű multiplexitás
> > > A telefonhálózatok így működnek, régen emberekkel ment, ma autómatizált
> > > Switch-eken keresztül is létezik, ígényt benyújtja valaki,
> > > a switchek kialakítják az *áramkört*
> > > *Netes pl: ATM*
> > > Overheadje van és a burst-ös kihasználtság még rontja a hatékonyságot
> > > Meghibásodás eset újra kell építeni az áramkört
> > > egyszerű, kiszámítható switch-ek
> >
> > ### Igény szerint
> >
> > > Akkor küld az adatot amikor kell
> > > Csomag szintű multiplexitás
> > > Az internet megy így, csaomagkapcsolt hálózatként reprezentált
> > > Bufferek használata, és csomagok tárolása szükséges
> > > Afkol néhány csomag teljes kihasználtság esetén
> > > Csomag fejlécinformáció feldolgozása overheadet ad
> > > Hatékony erőforráskihasználás
> > > Magas hibatolerancia
> > > kiszámíthatatlan teljseítmény
> >
> > ### Melyik a jobb?
> >
> > > Ha megvan a kellő sávszélesség akkor nem releváns a kérdés *(no shit)*
> > > Lefoglalás esetén mivel megeshet hogy egy adott Adatfolyam nincs
> > > elengedve, kihasználatlanul tud maradni a rendszer.
> > > Viszont ha egy adatfolyam kihasználná a lefoglalt kapacitást eléggé
> > > Ha az átlag adatfolyam nem használja ki a lefoglalt ráta nagyrészét
> > > Jobban járunk az on-dema###nd verzió a jobb
> > > Ez akkor tud előfordulni ha az adatfolyam kihasználtság löketekben történik
>
> ## Mi az internet
>
> > egy *bazinagy gráf*
> > a net az egy infrastruktóra, minden weblap csak egy
> > szolgáltatása a netnek, a net maga a hálózat
> > ISP-ken keresztül elérhetőek ezek a szoltáltatások
> >
> > > Tier-3: LAN (helyi) (az internet nagyon nagy része)
> > > Tier-2: Hálózatok a csomópontjai (nemzeti) (pár ezer)
> > > Tier-1: Nincs szolgáltatója, mindenki mindenkivel össze
> > > van kötve (világ) (pár tucat)
> > > Vannak peer összekötések, két szolgáltató megegyezik abban,
> > > hogy adatforgalmat hajlandóak kicserélni *(később részletezze)*
