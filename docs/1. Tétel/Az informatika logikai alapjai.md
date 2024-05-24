
### Elsőrendű logika szintaxisa és szemantikája

#### Elsőrendű logika szintaxisa

Az elsőrendű logika (First-Order Logic, FOL) kifejezőereje nagyobb, mint a kijelentéslogikáé, mert kvantorokat és predikátumokat is tartalmaz. Az elsőrendű logika szintaxisa a következő elemekből áll:

- **Konstansok**: Objektumok nevei (pl. `a`, `b`, `c`).
- **Változók**: (pl. `x`, `y`, `z`).
- **Függvényszimbólumok**: Olyan szimbólumok, amelyek egy vagy több objektumot vesznek és egy új objektumot eredményeznek (pl. `f(x)`).
- **Predikátumszimbólumok**: Olyan szimbólumok, amelyek egy vagy több objektumot vesznek és egy igazságértéket adnak vissza (pl. `P(x)`, `Q(x, y)`).
- **Logikai kapcsolók**: `¬` (negáció), `∧` (és), `∨` (vagy), `→` (implikáció), `↔` (ekvivalencia).
- **Kvantorok**: `∀` (minden), `∃` (létezik).

#### Elsőrendű logika szemantikája

Az elsőrendű logika szemantikája leírja, hogyan értelmezzük a logikai formulákat egy adott modellben:

- **Domén (D)**: Az objektumok halmaza, amelyekről a logika beszél.
- **Értelmezés (I)**: Egy függvény, amely hozzárendeli a konstansokhoz a domén elemeit, a függvényszimbólumokhoz függvényeket, és a predikátumszimbólumokhoz relációkat a domén felett.
- **Igazságérték hozzárendelése**: A logikai formulák értékelése az értelmezés és a változók hozzárendelése alapján történik.

### Normálformák elsőrendű logikában

A normálformák segítenek az elsőrendű logikai formulák egyszerűsítésében és feldolgozásában.

#### Konjunktív normálforma (CNF)

Egy formula konjunktív normálformában (CNF) akkor van, ha az alábbi formában írható:

\[ (L_{11} \vee L_{12} \vee \ldots \vee L_{1k}) \wedge (L_{21} \vee L_{22} \vee \ldots \vee L_{2m}) \wedge \ldots \wedge (L_{n1} \vee L_{n2} \vee \ldots \vee L_{np}) \]

ahol \( L_{ij} \) literálok, vagyis predikátumok vagy azok negációi.

#### CNF-re hozás algoritmusa

1. **Előzárójelzés**: Távolítsuk el az ekvivalenciát (\( \leftrightarrow \)) és az implikációt (\( \rightarrow \)).
2. **Negációk bejuttatása**: Alkalmazzuk a De Morgan törvényeket és duplikált negációk megszüntetése.
3. **Kvantorok mozgatása**: Minden kvantort vigyünk a megfelelő helyre (pl. a formula elejére).
4. **Skolemizáció**: A létezési kvantorok eltávolítása és a megfelelő Skolem-függvények bevezetése.
5. **Disztribúció**: Használjuk a disztributivitás szabályait a diszjunkciók és konjunkciók megfelelő átrendezéséhez.

### Skolemizáció

A Skolemizáció egy olyan technika, amely a létezési kvantorokat eltávolítja és Skolem-függvényekkel helyettesíti őket, így a formula csak univerzális kvantorokat tartalmaz. 

Például, a \( \forall x \exists y P(x, y) \) formulát a \( \forall x P(x, f(x)) \) formulával helyettesítjük, ahol \( f \) egy Skolem-függvény.

### Rezolúció elsőrendű logikában, unifikáció

#### Rezolúció

A rezolúció egy következtetési módszer, amely két klózt egyesít egy közös literál segítségével. 

Például, ha két klóz \( (A \vee B) \) és \( (\neg A \vee C) \), akkor a rezolúció eredménye \( (B \vee C) \).

#### Unifikáció

Az unifikáció olyan folyamat, amely két logikai kifejezést egy közös kifejezésbe egyesít változók megfelelő helyettesítésével.

Például, az \( P(x, f(y)) \) és \( P(a, f(z)) \) unifikálható a \( \{ x \mapsto a, y \mapsto z \} \) helyettesítési függvénnyel.

### Lineáris és SLD rezolúció

#### Lineáris rezolúció

A lineáris rezolúció egy speciális rezolúciós forma, ahol minden egyes rezolúció csak egy előző rezolúciós lépésből származó klóz és a kezdeti klózok egyike között történik.

#### SLD rezolúció

Az SLD (Selective Linear Definite clause) rezolúció a Prolog alapját képezi. Ez egy specializált rezolúciós módszer, amelyet a Horn-klózok felhasználásával végeznek.

### Prolog alapok

A Prolog (Programming in Logic) egy logikai programozási nyelv, amely az elsőrendű logikán alapul. A Prolog programok tényekből, szabályokból és lekérdezésekből állnak.

#### Prolog program felépítése

1. **Tények**: Alapállítások, amelyek mindig igazak. Például: `szülő(anna, béla).`
2. **Szabályok**: Olyan állítások, amelyek más állítások igazságától függenek. Például: `nagyszülő(X, Z) :- szülő(X, Y), szülő(Y, Z).`
3. **Lekérdezések**: Kérdések a tények és szabályok alapján. Például: `?- nagyszülő(anna, Z).`

A Prolog programozás alapelve a lekérdezések logikai következtetés útján történő megoldása rezolúció és unifikáció segítségével.

