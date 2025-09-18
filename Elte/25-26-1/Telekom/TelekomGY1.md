# [Canvas](https://canvas.elte.hu/courses/57748/pages/savszelesseg-es-kesleltetes-szamolas)

## Alapfogalmak

- Bandwidth
- Latency
- Jitter
- Utilisation

## Prefixek

> 1B -> 8b

## Késleltetés

- Propagation
- Serialisation
- Processing
- Queuing

## Egyszerű feladatok

> ### Átvitel idő
>
> Mennyi idő alatt továbbítunk 50 MB adatot egy 100 Mbit/s linken (overhead nélkül)?
>
> > 50 * 8 / 100 = 4s
>
> ### Propagációs késés
>
> Mennyi a terjedési késleltetés 200 km hosszú optikai szálon (5 μs/km)?
>
> > 200\*5 = 1 m
>
> ### RTT becslés
>
> Egy adatcsomag 1000 km szálon halad (5 μs/km). Becsüld meg az RTT-t,
> úgy hogy a hálózati eszközök feldolgozása további fix
> 2ms késleltetést ad irányonként!
>
> > 1000\*5 = 5ms
> > (5+2)\*2
>
> ### Hasznos hatásfok
>
> Maximális csomagméret(MTU) = 1500 B, ebből az IP fejléc (min):
> 20 B, TCP fejléc (min): 20 B. Számoljuk ki a hasznos hatásfokot százalékban.
> Mennyi a goodput 1 Gbps linken?
>
> > E = 1460 / 1500 ~= 97,3%
> > 1000Mbps\*0,973=973Mbps

## Komplex feladatok

> ### Adatközpont költöztetés – hálózati mentés vs. fizikai szállítás
>
> > Egy adatközpontot 3000 km-rel arrébb kell költöztetni.
> > A teljes adatállomány mérete legyen V (TB). Két lehetséges módszer:
> >
> > #### Hálózati adatmentés (dedikált kapcsolat)
> >
> > > Egyszeri beállítási díj: 500 €
> > > Adatforgalmi díj: 20 €/TB
> > > Összköltség:
> > > Cnet(V)=500+20V [€]
> >
> > #### Fizikai szállítás (lemezek + futár + biztosítás)
> >
> > > Egyszeri csomagolás/biztosítás/szállítás: 2000 €
> > > Kezelési/anyagköltség: 5 €/TB
> > > Összköltség:
> > > Cphys(V)= 2000+5V [€]
> >
> > #### Melyik módszer olcsóbb 40 TB és 300 TB esetén? Számold ki a költségeket
> >
> > > 40
> > >
> > > > 500 + 800 = 1300
> > > > 2000 + 200 = 2200
> > >
> > > 300
> > >
> > > > 500 + 6000 = 6500
> > > > 2000 + 1500 = 3500
> >
> > #### Mekkora V\* adatméretnél azonos a két módszer költsége?
> >
> > > 1500 - 15x = 0
> > > x = 100TB
