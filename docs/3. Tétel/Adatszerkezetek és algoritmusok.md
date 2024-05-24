# Adatszerkezetek és algoritmusok

## Algoritmus hatékonyságát befolyásoló algoritmizálási és adatkonstrukciós szempontok

Az algoritmusok hatékonysága kulcsfontosságú szempont a számítástechnika területén. Az alábbi tényezők befolyásolják egy algoritmus hatékonyságát:

1. **Időbeli komplexitás (Time Complexity)**: Az algoritmus futási idejének növekedése a bemeneti adatok méretének függvényében. Gyakran használják a Big O jelölést ennek kifejezésére (pl. O(n), O(log n)).
2. **Térbeli komplexitás (Space Complexity)**: Az algoritmus által használt memória mennyisége a bemeneti adatok méretének függvényében.
3. **Algoritmus struktúrája**: Az algoritmus lépéseinek és döntési pontjainak szerkezete.
4. **Adatszerkezet kiválasztása**: A megfelelő adatszerkezet kiválasztása jelentősen befolyásolja az algoritmus hatékonyságát.

## Dinamikus adatszerkezetek

Dinamikus adatszerkezetek olyan adattárolási struktúrák, amelyek képesek futás közben változtatni a méretüket. Az alábbiakban néhány fontos dinamikus adatszerkezetet és azok kezelését tárgyaljuk.

### Verem (Stack)

A verem egy LIFO (Last In, First Out) elven működő adatszerkezet. 

- **Műveletek**:
  - `push`: Elem hozzáadása a verem tetejére.
  - `pop`: Elem eltávolítása a verem tetejéről.
  - `peek`: A verem tetején lévő elem lekérdezése anélkül, hogy eltávolítanánk.
  
- **Implementáció**: Általában tömbbel vagy láncolt listával valósítják meg.

### Sor (Queue)

A sor egy FIFO (First In, First Out) elven működő adatszerkezet.

- **Műveletek**:
  - `enqueue`: Elem hozzáadása a sor végére.
  - `dequeue`: Elem eltávolítása a sor elejéről.
  - `front`: A sor elején lévő elem lekérdezése anélkül, hogy eltávolítanánk.

- **Implementáció**: Általában tömbbel vagy láncolt listával valósítják meg.

### Lista (List)

A lista egy olyan adatszerkezet, amely elemek sorrendjét tartja fenn, és lehetővé teszi az elemek hozzáadását, eltávolítását és módosítását.

- **Műveletek**:
  - `insert`: Elem beszúrása adott pozícióra.
  - `delete`: Elem eltávolítása adott pozícióról.
  - `find`: Elem keresése a listában.

- **Implementáció**: Általában tömbökkel vagy láncolt listákkal valósítják meg.

### Hash-tábla (Hash Table)

A hash-tábla egy kulcs-érték párokat tároló adatszerkezet, amely gyors keresést, beillesztést és törlést tesz lehetővé.

- **Műveletek**:
  - `insert`: Kulcs-érték pár hozzáadása.
  - `delete`: Kulcs-érték pár eltávolítása.
  - `search`: Érték keresése a kulcs alapján.

- **Implementáció**: Általában tömbökkel és hash függvényekkel valósítják meg.

## Kereső algoritmusok és hatékonyságuk

A kereső algoritmusok célja egy adott elem megtalálása egy adatszerkezetben. Néhány gyakori kereső algoritmus:

1. **Lineáris keresés (Linear Search)**: Sorban végigmegy az adatszerkezet minden elemén, amíg meg nem találja a keresett elemet. Időbeli komplexitása O(n).
2. **Bináris keresés (Binary Search)**: Keresési algoritmus rendezett tömbökben. Az adatszerkezet közepén kezd, és felezi a keresési területet minden lépésben. Időbeli komplexitása O(log n).

## Programozási tételek értelmezése különböző homogén adatszerkezetek esetében

Programozási tételek olyan általános megoldási minták, amelyek különböző problémákra alkalmazhatók. Homogén adatszerkezetek (azonos típusú elemeket tartalmazó adatszerkezetek) esetében ezek a tételek gyakran használatosak:

1. **Összegzés tétele**: Egy adatszerkezet elemeinek összegzése.
2. **Számlálás tétele**: Egy adatszerkezet elemeinek számlálása egy adott feltétel alapján.
3. **Maximum kiválasztás tétele**: A legnagyobb elem kiválasztása egy adatszerkezetből.
4. **Minimum kiválasztás tétele**: A legkisebb elem kiválasztása egy adatszerkezetből.

## Rekurzió

### Rekurzió és iteráció

A rekurzió egy olyan módszer, ahol egy függvény önmagát hívja meg egy probléma megoldása érdekében. Az iteráció ezzel szemben ciklusok (for, while) használatával oldja meg a problémát. Mindkét módszernek megvannak a maga előnyei és hátrányai.

### Fa adatszerkezet és műveletei

A fa egy hierarchikus adatszerkezet, amely csomópontokból áll. Minden csomópontnak lehetnek gyermek csomópontjai.

- **Műveletek**:
  - `insert`: Elem hozzáadása a fához.
  - `delete`: Elem eltávolítása a fából.
  - `search`: Elem keresése a fában.
  - `traversal`: A fa bejárása (in-order, pre-order, post-order).

A fák speciális típusai közé tartozik a bináris fa, bináris keresőfa, AVL fa és a piros-fekete fa.