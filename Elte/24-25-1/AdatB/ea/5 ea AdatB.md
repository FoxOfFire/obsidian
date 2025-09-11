tranzakció kezelés
paralel interakciókat le kell kezelni
sorbarendezhetőség -> fontos hogy legyen műveleti sorrend az egyes lekérdezések közt
nem feltétlen garantálható a soros művelet elvégzés
> lassítaná nagyon a műveletis sebességet
> ACID -> valami rövidítés
> rollback -> tranzakcó előtti állapot visszaállítása
> vannak furcsa átfedések, edge case-ed
> (min)(max), (del)(ins) utasításokat érdemes egy tranzakcióba szervezni
> tranzakció implementácio nem standard, történelmi okokból
> tranzakció szigorúság választható a felhasználó által
>> read uncommited -> nem végleges/ később abortáló infókat is ki tud olvasni
>> read commited -> végleges adatok de nem feltétlen konzisztens
>> repeatable read -> egyel koznisztensebb, de a *fantom adatok* ellen nem véd xd
>> sorbarendezhető -> konzisztens, de lehet lassú

nézettáblák
>??
>virtuális -> le van kérdezve de nem tárolódik csak relációt ad meg
>materializált -> kiszámolódik és eltárolódik, gyakranhasznált tábláknál előnyös
>materializált tábla frissítés költséges
>napi/heti téma pl canvason hajnalban frissül
>adattárház -> mother adatbázis nézettáblákra épül

indexek
>segédadatstruktúra az adatbázis mellet ami a hatékony keresést segíti elő
>
>tuning
>>attől függöen hogy hogy használod a táblát kell kiválasztani az indexet
>>rossz indexválasztás lassítja az adatbázis általános működését
>>***Adatbázis hangolási szakértők*** xddd
>>AI hangolás gyakori manapság

jogosultságkezelés (authorization)
>9 jogosultság
>notable:
>>SELECT -> akár csak egy atribútumra vonotkozhat
>>INSERT -> akár csak egy atribútumra vonotkozhat
>>DELETE
>>UPDATE -> akár csak egy atribútumra vonotkozhat
>>REFERENCE -> blokkolási problémákat okoz az alap és a továbbgyűrűzés is
>
>
