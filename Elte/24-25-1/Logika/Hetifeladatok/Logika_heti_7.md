Készítsünk ítéletkalkulusbeli levezetést a következő szintaktikus eldöntésproblémához!
{¬X ∧ ¬¬Y } |- Y ∧ X ⊃ Z
dedukciós tétel:
{¬X∧¬¬Y, Y∧X} |-Z

1. ¬X∧¬¬Y [Hip]
1. Y∧X [Hip]
1. Y∧X>X [B2,A||Y,B||X]
1. ¬¬Y∧¬X>¬X [B2,A||¬¬Y,B||¬X]
1. X [mp(2,3)]
1. ¬X [mp(1,4)]
1. (¬Z>X)>(¬Z>¬X)>Z [A3,A||Z,B||X]
1. X>(¬Z>X) [A1,A||X,B||¬Z]
1. (¬Z>X) [mp(5,8)]
1. (¬Z>¬X)>Z [mp(7,9)]
1. ¬X>(¬Z>¬X) [A1,A||¬X,B||¬Z]
1. (¬Z>¬X) [mp(6,11)]
1. Z [mp(10,12)]
