\[[Logika 3]\]ra nem jöttem be lol
\[[Logika 2]\] volt így az előző

> ______________________________________________________________________
>
> Zh gyak időben
> {¬Y ∨ Z, ¬(Z ∧ ¬X) ∧ Y} |= X

| X | Y | Z | ¬Y ∨ Z | ¬(Z ∧ ¬X) ∧ Y | X |
| --- | --- | --- | ------ | ------------- | --- |
| i | i | i | i | i | i |
| i | i | h | h | i | i |
| i | h | i | i | h | i |
| i | h | h | i | h | i |
| h | i | i | i | h | h |
| h | i | h | h | i | h |
| h | h | i | i | h | h |
| h | h | h | i | h | h |

> ## A következmény teljesül:) (nem kielégíthető hanem teljesül)

\[[Tablókalkulus]\] Szabályait alkalmazzuk majd:

> ______________________________________________________________________
>
> - {(X ⊃ Y) ∧ (X ⊃ Z), X} |= Y ∧ Z
> - {¬X ∨ ¬Y} |= ¬(X ∧ Y)
> - {X ∨ (Y ∧ Z)} |= (X ∨ Y) ∧ (X ∨ Z)
>
> ______________________________________________________________________
>
> T (¬Y v Z) ∧ ¬(Z ∧ ¬X) ∧ Y ∧ ¬X
> |
> T (¬Y v Z)
> |
> T ¬(Z ∧ ¬X)
> |
> T Y
> |
> T ¬X
> |
> F X
> |
> F Z ∧ ¬X -> (2)
> |
> T (¬Y)
> |
> F Y \<\*>

(2)
|
mmmmmmmmmmm

> ______________________________________________________________________
>
> ezt érdemes füzetben xdd
> a gráfkészítés nem annyira lehetséges itt :(
>
> ______________________________________________________________________
>
> {(X ⊃ Y) ∧ (X ⊃ Z), X} |= Y ∧ Z
> \[[Eldöntés Probléma]\] tétele
> F (X ⊃ Y) ∧ (X ⊃ Z) ⊃ X ⊃ Y ∧ Z

______________________________________________________________________

> TODO
>
> - T (∀x∃yQ(x,y) ⊃ ∀xP(x)) ∧ ¬∀xP(x) ∧ ∀x∃yQ(x,y)

∀ ∃
∧ ∨ ⊃ ¬
