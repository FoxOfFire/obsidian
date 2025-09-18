# logika heti 2

Prev: \[[Logika_heti_1]\]
E -> eszek levest
F -> aztmondom hogy finom a leves
D -> kapok deszertet

1 D ⊃ (E ∨ F)
¬(F ∧ ¬D)
¬(E ⊃ D)
E ∧ (F ⊃ D)

igazolás *(markdown)* táblázattal
{D ⊃ (E ∨ F), ¬(F ∧ ¬D),¬(E ⊃ D)} ⊨ E ∧ (F ⊃ D)

| E | F | D | D ⊃ (E ∨ F) | ¬(F ∧ ¬D) | ¬(E ⊃ D) | E ∧ (F ⊃ D) |
| --- | --- | --- | ----------- | --------- | -------- | ----------- |
| i | i | i | i | i | h | i |
| i | i | h | i | h | i | h |
| i | h | i | i | i | h | i |
| i | h | h | i | i | i | i |
| h | i | i | i | i | h | h |
| h | i | h | i | h | h | h |
| h | h | i | h | i | h | h |
| h | h | h | i | i | h | h |

a formula az igazságtáblázat 4 srában kielégíthető ezért {1,2,3} ⊨ 4
