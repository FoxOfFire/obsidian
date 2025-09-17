# Ea1 *(ismétlés főleg :( )*

## Fogalmak

> ábécé -> nemíüres betűk halmaza
> szavak -> ábécé betüiból összerakott tetszőleges sorozat
> szóhossz -> betűk száma kivéve *E*
> nyelv -> szavak egy adott halmaza egy ábécé felett
> nyelvcsalád -> nyelv hatványhalmazának részhalmaza *(?)*
> grammatika -> G = \<N,T,P,S> *(nemterminális, terminális, szabályok, kezdőszimbólum)*
> levezethetőség -> szabályalkalmazások sorozatából elkészíthető a szó

### grammatika osztályzás

> 0 -> nincs szabály
> 1 -> a környezetfüggö, korlátozott epszilon szabályok
> 2 -> környezet független
> 3 -> reguláris kifejezés azaz A->uB | u
> ha egy nyelv generálható n-típusu grammatikával az n-típusu nyelv lesz
> Chomsky nyelvhierarchia -> L3\<L2\<L1\<L0

### Veremautómata

> A = \<Z,Q,T,d,z0,q0,F>
>
> Z -> veremszimbólumok halmaza
> Q -> állapotok halmaza
> T -> input szimbólumok véges halmaza
> d -> átmeneti függvények halmaza
> z0 -> kezdeti veremszimbólum
> q0 -> kezdeti állapot
> T -> elfogadható állapotok halmaza
> Állapot: zqw -> (veremelem, állapot, feldolgozatlan rész)
> n lépéses redukció xd
> lehet egy automata determinisztikus is, illetve parciálisan determinisztikus,
> ha bizonyos állapot kombókra nincs szabály
