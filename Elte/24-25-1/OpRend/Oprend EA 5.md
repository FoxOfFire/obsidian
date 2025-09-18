# oprend ea 5

Prev: \[[Oprend EA 4]\]
cfq

> xd

ütemezés kulcsfeladata:

> sávszélesség a lemez közepén a legnagyobb
> defragmentation
> közép gyors xd
> lemezgyorsítótár memóriában

os rendszerszolgáltatások:

> dinamikus kötet- több lemezre helyezett logikai meghajtó
> tükrözés- két lemezre tett paralel tükörmeghalytók
> nagy(obb) cpu igény

hardware szolgáltatás

> intelignes meghajtó szolgáltatás
> Az SCSI eszköz világámban jelent meg először a RAID

RAID -> rendundant array of inexpensive disks

> ha os nyújtotta SoftRaid
> ha külső vezérlő egység csinálja, hardver Raid
> csak theoretically olcsó
> több egységet összefogó egy lemeznek látja
> RAID 0
>
> > striping
> > sok lemezt egy nagy egységnek látja
> > logikai meghajtó több helyre lesz szétbontja
> > gyorsított i/o
>
> RAID 1
>
> > tükrözés
> > felezett tárolás:(
> > drága lol
> > hibatűrő megoldást -> csak ha mindkettő behal van baj
>
> Raid kombinált
>
> > 0+1
> > 1+0
>
> RAID 2
>
> > adatbit+javítóbitek
> > ecc -> Erroc correction code
>
> RAID 3
>
> > elég 1 extra paritásdiszk
>
> RAID 4
>
> > RAID 0 + paritásdiszkek
>
> ma 2,3,4 nem gyakori
>
> RAID 5
>
> > RAID 3 hoz hasonló csak a paritás diszk szét van szórva a többi közt
> > inteso cpu használat
> > redundáns tárolás -> 1 diszk vesztés != adatvesztés
> >
> > > legalább 3 diszk
> >
> > n + 1 diszk -> n diszknyi adattárolási potenciál
>
> RAID 6
>
> > RAID 1, 5 gyakoribb
> > ecc
> > hot swap -> nem kell leállítani a szervert hogy diszket cseréljünk
> > spare disk -> tartalék diszk a tömbben

SCSI -> small copmuter system interface

> SAS, SATA a modern alternatívája

Next up

> filerendszerek

fájlok

> infotároló egység
> név
> egyéb atribútumok pl méret tulaj rejtett stb
> elhelyezés
>
> > valós
> > link(hard)
> > link(soft)

könyvtárak

> no rendzser
> katalógus egy, kétszintű
> többszintű hierarchikus
>
> > hatékony
> > fa struktúra
> > mai
>
> abszolút relatív hivatkozás
