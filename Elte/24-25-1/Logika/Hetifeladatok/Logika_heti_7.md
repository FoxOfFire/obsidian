Készítsünk ítéletkalkulusbeli levezetést a következő szintaktikus eldöntésproblémához!
{¬X ∧ ¬¬Y } |- Y ∧ X ⊃ Z
dedukciós tétel:
{¬X∧¬¬Y, Y∧X} |-Z
1. ¬X∧¬¬Y [Hip]
2. Y∧X [Hip]
3. Y∧X>X [B2,A||Y,B||X]
4. ¬¬Y∧¬X>¬X [B2,A||¬¬Y,B||¬X]
5. X [mp(2,3)]
6. ¬X [mp(1,4)]
7. (¬Z>X)>(¬Z>¬X)>Z [A3,A||Z,B||X]
8. X>(¬Z>X) [A1,A||X,B||¬Z]
9. (¬Z>X) [mp(5,8)]
10. (¬Z>¬X)>Z [mp(7,9)]
11. ¬X>(¬Z>¬X) [A1,A||¬X,B||¬Z]
12. (¬Z>¬X) [mp(6,11)]
13. Z [mp(10,12)]