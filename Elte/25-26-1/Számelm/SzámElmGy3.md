# gy 3

maradék fonya

prev -> CYK
Véges determinisztikus autómata
A = (Q,T,d,q0,F)

van kezdőállapota
eltárol egy állapotot
egy irányban olvas csak
állot lehet elfogadható, vagy nem elfogadhatónak
d: QxT->Q
pl: *d(q0,a)=q1*

## VDA

> a =({q0,q1,q2},{a,b},d,q0,{q2}
> **d**
>
> - d(q0,a)=q1
> - d(q1,a)=q1
> - d(q1,b)=q1
>
> POV: gráf reprezentáció

## VNA

> van benne két különböző szabály ugyan olyan állapot bemenet kombóval
> példa ara hogy hogy fogad illetve nem fogad el egy szót egy lehetséges automata
> "ami rossz azt biztosan nem fogadja el, ami jó azt legalább egy levezetéssel elfogadja"
> d: QxT->L^Q *(Q összes részhalmaza)*

______________________________________________________________________

## Veremautómaták

> Tartalmaz:
>
> - Logika
> - Olvasófej
> - Verem (amiben van egy verem alja szimbólum lalapvetően, # )
>
> tud pop ot olvasni
> tud pusholni akár több elemet is
> *VDA + memória*
>
> A=(Z,*Q*,*T*,d,*q0*,z0,*F*)
> Z -> veremszimbólumok halmaza
> z0 -> Verem kezdőszimbólum (általában #)
> d: ZxQx{T*U*{*e*}->2^Z\*xQ(verem szimbólumok sorozataának és egy állapontan a hatványhalmaza)
> d(#,q0,a) = {(#abb,q1), *(a,q2)*, (*e*,q2)}
> müvelet fix poppol, és nem érdemes lecserélni a veremalja szimbólumot
> d(a,q2,*e*) =
> itt nem olvasunk a szallagról azaz verem manipuláció
>
> POV Gráfos leírás:(
>
> (veremtartalom,olvasott)->verem push
> (#,a)->#a
> -------->
>
> L(A)={U€T\*|Vq0U=>lr,v€Z\*,l€Z\*,r€F}
> N(A)={U€T\*|Vq0U=>p,v€Z\*,P€Q} (Kiürített verem és elfogyott input szallag => elfogadás)

## Feladatok

> ***L1 = {a^nb^n|n>=1} aaabbb***
>
> > **0**
> > (#,a)->#a 0
> > (a,a)->aa 0
> > (a,b)->*e* 1
> >
> > **1** *elfogadó állapot*
> > (a,b)->*e* 1
> >
> > **aaabbb levezetése**\*
> > #0aaabbb -> #a0aabbb -> #aa0abbb -> #aaa0bbb -> #aa1bb -> #a1b -> #1
>
> ***L2 = {UcU^-1|U€{a,b}+} abbcbba***
>
> > **0**
> > (#,a)->#a 0
> > (#,b)->#b 0
> > (a,a)->aa 0
> > (b,a)->ba 0
> > (a,b)->ab 0
> > (b,b)->bb 0
> > (#,c)->*e* 1
> > (a,c)->*e* 1
> > (b,c)->*e* 1
> >
> > **1** \*elfogadó állapot
> > (a,a)->*e* 1
> > (b,b)->*e* 1
> >
> > **abbcbba levezetése**
> > #0abbcbba -> #a0bbcbba -> #ab0bcbba -> #abb0cbba ->
> > -> #abb1bba -> #ab1ba -> #a1a -> #1
>
> L3 = {UU^-1|U€{a,b}+} abbaabba
>
> > **0**
> > (#,a)->#a 0
> > (#,b)->#b 0
> > (a,a)->aa 0
> > (b,a)->ba 0
> > (a,b)->ab 0
> > (b,b)->bb 0
> > (b,*e*)->b 1
> > (a,*e*)->a 1
> >
> > **1** \*elfogadó állapot
> > (a,a)->*e* 1
> > (b,b)->*e* 1
> >
> > **abbbba levezetése**
> > #0abbbba -> #a0bbbba -> #ab0bbba -> #abb0bba -> #abb1bba -> #ab1ba -> #a1a -> #1
>
> ***L4 = {U€{a,b}+|la(U)=lb(U)} abbaab***
>
> > **0**
> > (#,a)->#a 1
> > (#,b)->#b 2
> >
> > **1**
> > (a,a)->aa 1
> > (a,b)->*e* 1
> > (#,*e*)-># 3
> >
> > **2**
> > (b,b)->bb 2
> > (b,a)->*e* 2
> > (#,*e*)-># 3
> >
> > **3**
> > *elfogadó állapot*\*
