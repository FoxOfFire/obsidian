# log heti 6

{∃zR(a, z) ∨ ¬∃zQ(z), ¬∀zQ(z)} |= ¬∃xR(a, x)

visszakövetkeztetéssel állapítsuk meg hogy az alábbi formulahalmaz kielégíthetetlen-e:
{∃zR(a, z) ∨ ¬∃zQ(z), ¬∀zQ(z),¬∃xR(a, x)}

I((∃zR(a, z)∨¬∃zQ(z)) ∧ ¬∀zQ(z) ∧ ¬∃xR(a, x)) (α) (1)
|
I (∃zR(a, z)∨¬∃zQ(z)) [1] (β) (4)
|
I ¬∀zQ(z) [1] (α) (2)
|
I ¬∃xR(a, x) [1] (α) (3)
|
H ∀zQ(z) [2] (δ) (6 z||b)
|
H ∃xR(a, x) [3] (γ) (8,x||c)
|
I ∃zR(a, z) [4] (δ) (7,z||c) , I ¬∃zQ(z) [4] (α) (5)-> *xd*
|
H Q(b) [6]
|
I R(a,c) [7]
|
H R(a,c) [8]
-ellentmondás

*xd*
|
H ∃zQ(z) [5] (γ) (9 z||b)
|
H Q(b) [6]
|
H R(a,c) [8]
|
H Q(b) [9]

nincs ellentmondás -> a formula halmaz kielégíthető
ezért a szemantikus következmény teljesül
