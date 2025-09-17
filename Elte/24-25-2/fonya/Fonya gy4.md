## 5.órai feladatok

______________________________________________________________________

### 1

*Szintaktikus elemző*

- S -> neE | nc
- E -> veE | C
- C -> c
  *Lexikális elemző*
- '\[' -> n
- [a-zöi]+ -> e
- ',' -> v
- '\]' ->c

> [alma,körte,szilva] (->nevevec (->S (✅)))))

______________________________________________________________________

### 2

char etuje( string s, int index);
int osszeg( int x, int y,);

*Lexikális elemző*

- [a-z]+ -> a

- '(' -> n

- ')' -> c

- ',' -> v

- ';' -> p

- [ \\n] ->

- . -> LEXERROR

*Szintaktikus elemző*

- S -> L | ε
- L -> LL | A
- A -> aanBcp | aancp
- B -> aa | aavB

______________________________________________________________________

### 3

blokkszerkezet leírása
begin
skip\
end

*Lexickális elemző*

- "begin" -> b
- "end" -> e
- "skip" -> s
- [ \\n] ->
- . -> LEXERROR

*Szintaktikus elemző*

- S -> ε | A
- A -> AA | B | bAe
- B -> s | ε

> *vagy*
> S -> ε | sS | bSeS

______________________________________________________________________

### 4

ha páros akkor páratlan := !kulcsszó
*Lexickális elemző*

- "!"[a-z0-9]+ -> var
- "ha" -> ha
- "akkor" -> akkor
- "kezd" -> begin
- "vege" -> end
- "paros" -> paros
- "paratlan" -> paratlan
- ":=" -> ert_ad
- "+" -> plus
- "-" -> minus
- [0-9]+ -> szam
- [ \\n] ->
- . -> LEXERROR

*Szintaktikus elemző*

- S -> STATEMENTS | ε
- STATEMENTS -> STATEMENT STATEMENTS | STATEMENT
- STATEMENT -> ASSIGN | IF
- ASSIGN -> var er_tad ERTEK
- IF -> ha ERTEK akkor ASSIGN | ha ERTEK akkor begin STATEMENTS end
- ERTEK -> var | szam | ERTEK plus ERTEK | ERTEK minus ERTEK | ERTEK paros | ERTEK paratlan
