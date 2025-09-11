Prev:[[Logika_heti_2]]
- Az összes téli hónap hideg, és januárban csapadék is esik.
- Létezik olyan nyári hónap, amikor csapadék is esik, vagy melegrekord dől.
- A február előtti hónap hideg, a február utáni hónapban pedig nem dől melegrekord

Univerzum: {hónapok}
Predikátum szimbólumok:
- H(x) -> x hideg hónap
- M(x) -> x hónap alatt melegrekord dőlt
- T(x) -> x téli hónap
- N(x) -> x nyári hónap
- E(x) -> x hónap alatt esett csapadég

Konstansok:
- j᷉ -> janurár
- f᷉ -> február

Függvények:
e(x) -> megadja x előtti hónapot
u(x) -> megadja x utáni hónapot

Interpretációk:
- ∀x(T(x) ⊃ H(x)) ∨ E(j᷉) 
- ∃x(N(x) ⊃ (M(x) ∨ E(x)))
- H(e(f᷉)) ∧ ¬M(u(f᷉)) 


∀  ∃
∧ ∨ ⊃ ¬
