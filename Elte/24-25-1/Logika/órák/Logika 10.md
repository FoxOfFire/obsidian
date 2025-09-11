zh gyak lol
# ítélet:
### {!P>Q,Q>R,!R} |- P
1. !P>Q [hip]
2. Q>R [hip]
3. !R [hip]
4. (!P>R)>(!P>!R)>P [A3,A||P,B||R]
5. (!P>Q)>((Q>R)>(!P>R)) [B2,A||!P,B||Q,C||R]
6. (Q>R)>(!P>R) [mp(1,5)]
7. (!P>R) [mp(2,6)]
8. (!P>!R)>P [mp(4,7)]
9. !R>(!P>!R) [A1,A||!R,B||!P]
10. !P>!R [mp(3,9)]
11. P [mp(8,10)]


### {!!D,D>!F,(E>F)^F} |- !E
1. !!D [hip]
2. D>!F [hip]
3. (E>F)^F[hip]
4. !!D > D [B4,A||D]
5. D [mp(1,4)]
6. !F [mp(2,5)]
7. (E>F)^F>(E>F)
8. E>F [mp(3,7)]
9. (!!E>!F)>(!!E>!!F)>!E [A3,A||!E,B||!F]
10. !F>(!!E>!F) [A1,A||!F,B||!!E]
11. !!E>!F [mp(6,10)]
12. (!!E>!!F)>!E [mp(9,11)]
13. (E>F)>(!!E>!!F) [B5,A||E,B||F]
14. !!E>!!F [mp(8,13)]
15. !E [mp(12,14)]


### {!Y^(!!X>!Z),!Z>!(Xv!Y)} |- Z
1. !Y^(!!X>!Z) [hip]
2. !Z>!(Xv!Y) [hip]
3. !Y^(!!X>!Z) > !Y [C2,A||!Y,B||(!!X>!Z)]
4. !Y^(!!X>!Z) > (!!X>!Z) [C3,A||!Y,B||(!!X>!Z)]
5. !Y [mp(1,3)]
6. !!X>!Z [mp1,4]
7. (!!X>!Z)>(!Z>!(Xv!Y))>(!!X>!(Xv!Y)) [B2,A||!!X,B||!Z,C||!(Xv!Y)]
8. (!Z>!(Xv!Y))>(!!X>!(Xv!Y)) [mp(6,7)]
9. !!X>!(Xv!Y) [mp(2,8)]
10. (!Z>!Y)>(!Z>!!Y)>Z [A3,A||Z,B||!Y]
11. !Y>(!Z>!Y) [A1,A||!Y,B||!Z]
12. !Z>!Y [mp(5,11)]
13. (!Z>!!Y)>Z [mp(10,12)]
14. !Y>(Xv!Y) [D2,A||!Y,B||X]
15. Xv!Y [mp(5,14)]
16. (!Z>!(Xv!Y))>(!Z>Xv!Y)>Z [A3,A||!Z,B||(Xv!Y)]
17. (!Z>Xv!Y)>Z [mp(2,16)]
18. Xv!Y>(!Z>Xv!Y) [A1,A1||Xv!Y,B||!Z]
19. !Z>Xv!Y [mp(15,18)]
20. Z [mp(17,19)]

bruh

### {!Y^(!!X>!Z),!Z>!(Xv!Y)} |- Z
1. !Y^(!!X>!Z) [hip]
2. !Z>!(Xv!Y) [hip]
3. !Y^(!!X>!Z) > !Y [C2,A||!Y,B||(!!X>!Z)]
4. !Y [mp(1,3)]
5. !Y>(Xv!Y) [D2,A||!Y,B||X]
6. Xv!Y [mp(4,5)]
7. !Z>!(Xv!Y))>(!Z>Xv!Y)>Z [A3,A||!Z,B||(Xv!Y)]
8. (!Z>Xv!Y)>Z [mp(2,7)]
9. Xv!Y>(!Z>Xv!Y) [A1,A1||Xv!Y,B||!Z]
10. !Z>Xv!Y [mp(6,9)]
11. Z [mp(8,10)]

# Természetes
### {!P>Q,Q>R,!R} |- P
 !P>Q,Q>R,!R,!P,Q |- Q>R (azon) ; !P>Q,Q>R,!R,!P,Q |- Q (azon)
!P>Q,Q>R,!R,!P |- !P>Q (azon) ; !P>Q,Q>R,!R,!P |- !P (azon) ;  !P>Q,Q>R,!R,!P,Q |- R (>a); !P>Q,Q>R,!R,!P,Q |- !R(azon)
!P>Q,Q>R,!R,!P |- Q (>a); !P>Q,Q>R,!R,!P |- !Q (!b)
!P>Q,Q>R,!R |- !!P (!b)
!P>Q,Q>R,!R |- P (!a)



### {!!D,D>!F,(E>F)^F} |- !E
!!D,D>!F,E>F,F,E |- !!D (azon)
!!D,D>!F,E>F,F,E |- D (!a) ; !!D,D>!F,E>F,F,E |- D>!F (azon)
!!D,D>!F,E>F,F,E |- !F (>a); !!D,D>!F,E>F,F,E |- F (azon)
!!D,D>!F,E>F,F |- !E (!a)
!!D,D>!F,(E>F)^F |- !E (^A)



### {!Y^(!!X>!Z),!Z>!(Xv!Y)} |- Z
!Y, !!X>!Z, !Z>!(Xv!Y), !Z |- !Y (azon) ; !Y, !!X>!Z, !Z>!(Xv!Y), !Z |- !Z (azon) ; !Y, !!X>!Z, !Z>!(Xv!Y), !Z |- !Z>!(Xv!Y) (azon)
!Y, !!X>!Z, !Z>!(Xv!Y), !Z |- Xv!Y (vb);  !Y, !!X>!Z, !Z>!(Xv!Y), !Z |- !(Xv!Y) (>a)
!Y,!!X>!Z,!Z>!(Xv!Y) |- !!Z (!b) 
!Y,!!X>!Z,!Z>!(Xv!Y) |- Z (!a)
!Y^(!!X>!Z),!Z>!(Xv!Y) |- Z (^a)


# Szekvent
### {!P>Q,Q>R,!R} |- P
Q>R,P-> P,R(azon) ; Q -> Q,P,R (azon) ;  Q,R -> P,R (azon)
Q>R -> P,R,!P (->!) ; Q,Q>R -> P,R (>->)
!P>Q,Q>R -> P,R (>->)
!P>Q,Q>R,!R -> P (->!)


### {!!D,D>!F,(E>F)^F} |- !E
E>F,F,E,D -> F (azon)
E>F,F,E,D -> D (azon) ; !F,E>F,F,E,D -> (!->)
D>!F,E>F,F,E,D -> (>->)
D>!F,(E>F),F,E -> !D (->!)
!!D,D>!F,(E>F),F,E -> (!->)
!!D,D>!F,(E>F)^F,E -> (^->)
!!D,D>!F,(E>F)^F -> !E (->!) 


### {!Y^(!!X>!Z),!Z>!(Xv!Y)} |- Z
Y -> Z,Y,!!X, X (azon);!Z,Y -> Z,Y, X (azon)
-> Z,Y,!!X, X,!Y (->!);!Z -> Z,Y, X, !Y (->!) 
-> Z,Y,!!X, Xv!Y (->v); Z ->, Z,Y,!!X (azon) ;  !Z -> Z,Y, Xv!Y (->v)
!(Xv!Y) -> Z,Y,!!X  (!->); ->!Z, Z,Y,!!X  (->!);!(Xv!Y), !Z -> Z,Y ; !Z ->Z,Y,!Z (azon) 
!Z>!(Xv!Y) -> Z,Y,!!X ;(>->) !Z>!(Xv!Y),!Z -> Z,Y (>->)
!!X>!Z,!Z>!(Xv!Y) -> Z,Y (>->)
!Y,(!!X>!Z),!Z>!(Xv!Y) -> Z (!->)
!Y^(!!X>!Z),!Z>!(Xv!Y) -> Z (^->)