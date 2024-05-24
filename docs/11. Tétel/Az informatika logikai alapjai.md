# Az informatika logikai alapjai

## Nulladrendű logika szintaxisa és szemantikája

- **Szintaxis**: A nulladrendű logika szintaxisa az alapvető logikai összetevőket, például az atomi kifejezéseket (proposicionális változókat), a logikai összekötőket (pl. "és", "vagy", "nem"), valamint a zárójeleket foglalja magában.
- **Szemantika**: A nulladrendű logika szemantikája a logikai kifejezések értelmezésével és igazságértékével foglalkozik.

## Igazságtábla

Az igazságtábla egy táblázat, amelyben az összes lehetséges igazságértékek kombinációi szerepelnek az adott logikai kifejezés változóira vonatkozóan, valamint a kifejezés igazságértékét mutatja.

## Normálformák nulladrendű logikában

A normálformák olyan formák, amelyek megkönnyítik a logikai kifejezések értelmezését és elemzését. Néhány közismert normálforma a nulladrendű logikában:

- **Diszjunktív normálforma (DNF)**: A logikai kifejezés olyan diszjunkciója, amelyben az összes változó vagy annak negációja szerepel.
- **Konjunktív normálforma (KNF)**: A logikai kifejezés olyan konjunkciója, amelyben az összes változó vagy annak negációja szerepel.

## CNF-re hozás algoritmusa

A CNF-re hozás algoritmusa olyan módszer, amely átalakítja a logikai kifejezést konjunktív normálformába.

## Tseitin transzformáció és Plaisted-Greenbaum kódolás

A Tseitin transzformáció és a Plaisted-Greenbaum kódolás olyan módszerek, amelyek a proposicionális logikai kifejezéseket konjunktív normálformába alakítják.

## Rezolúció nulladrendű logikában

A rezolúció egy algoritmikus eljárás, amely a következtetésre épül, és a diszjunktív normálformában levő kijelentések egyszerűsítésére és következtetésre használják.

## SAT, DPLL és DIMACS

- **SAT (Boolean satisfiability problem)**: A kielégíthetőségi probléma, amely arra a kérdésre vonatkozik, hogy egy adott logikai kifejezés kielégíthető-e, azaz van-e olyan változó attribúció, amelyre az igazságérték igaz.
- **DPLL (Davis-Putnam-Logemann-Loveland) algoritmus**: Egy hatékony módszer a SAT probléma megoldására.
- **DIMACS (DIMensional ACcepted format)**: Egy standard formátum a Boole-algebrai kielégíthetőségi problémák leírására.

## SMT és SMT-LIB

- **SMT (Satisfiability Modulo Theories)**: A kielégíthetőség-modellolás olyan matematikai problémák megoldása, amelyek logikai kifejezéseket tartalmaznak más alapelméletekkel, például lineáris aritmetikával vagy bitvektorokkal.
- **SMT-LIB**: Egy nyelv a kielégíthetőség-modellolási problémák leírására és megoldására szolgáló szoftvereszközök és algoritmusok számára.