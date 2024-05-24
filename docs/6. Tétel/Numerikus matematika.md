# Numerikus matematika

## Hibák típusa, hibaterjedés

### Hibák típusai

1. **Lekerekítési hiba**: A számítógépek véges pontosságú számábrázolása miatt jelentkező hiba, amikor egy számot nem lehet pontosan ábrázolni, így az értéke lekerekítve kerül tárolásra.
   
2. **Truncálási hiba**: Az algoritmusban vagy matematikai módszerben alkalmazott közelítések miatt fellépő hiba. Például a Taylor-sorozat véges számú tagjának használata.

3. **Mérési hiba**: Az adatok méréséből vagy gyűjtéséből származó hiba, amely lehet véletlen vagy szisztematikus.

### Hibaterjedés

A hibaterjedés az a folyamat, amely során az adatokban vagy számításokban lévő hibák átterjednek és felerősödnek a számítások további lépései során. A hibaterjedést befolyásolhatja az alkalmazott numerikus módszer és az algoritmus stabilitása.

## Nemlineáris egyenletek megoldása

A nemlineáris egyenletek megoldására több numerikus módszer létezik:

1. **Bisection módszer**: Két kezdeti érték között, amelyek különböző előjelűek, iteratívan felezi az intervallumot, amíg el nem éri a kívánt pontosságot.
   
2. **Newton-Raphson módszer**: Egy iteratív módszer, amely a tangensvonalak metszéspontjait használja a gyökök közelítésére.

   ```math
   x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}
   ```

3. **Secant módszer**: Hasonló a Newton-Raphson módszerhez, de nem igényli a derivált kiszámítását. Két kezdő érték közötti szekáns vonalakat használja.

## Numerikus integrálás

A numerikus integrálás a határozott integrálok közelítő értékének meghatározása diszkrét pontok alapján.

1. **Trapéz módszer**: A függvényt trapézokkal közelíti.

   ```math
   \int_a^b f(x) \, dx \approx \frac{b - a}{2} [f(a) + f(b)]
   ```

2. **Simpson-módszer**: Parabolákkal közelíti a függvényt.

   ```math
   \int_a^b f(x) \, dx \approx \frac{b - a}{6} [f(a) + 4f(\frac{a + b}{2}) + f(b)]
   ```

## Lineáris egyenletrendszerek megoldása

A lineáris egyenletrendszerek megoldására több numerikus módszer létezik:

1. **Gauss-elimináció**: Az egyenletrendszert sorok összeadásával háromszög alakú mátrixra alakítja, majd visszahelyettesítéssel oldja meg.

2. **Gauss-Seidel iteráció**: Egy iteratív módszer, amely az egyenleteket egyenként oldja meg és az új értékeket azonnal felhasználja.

3. **LU-felbontás**: A mátrixot két háromszög mátrix szorzatára bontja (L és U mátrix), és ezeket használja a megoldásra.

## Függvénykiértékelés

A függvénykiértékelés numerikus módszerekkel történő megközelítése során az alapvető cél, hogy a lehető legpontosabban és hatékonyabban számítsuk ki a függvény értékét egy adott pontban. Különféle polinomiális és racionális közelítéseket alkalmazhatunk.

## Interpoláció

Az interpoláció célja egy függvény értékeinek becslése ismert pontok alapján.

1. **Lineáris interpoláció**: Két pont közötti értékek becslése egyenes vonallal.

2. **Polinomiális interpoláció**: Egy többfokú polinomot illeszt az ismert pontokra.

3. **Lagrange interpoláció**: Az ismert pontokon áthaladó polinomot határoz meg.

   ```math
   P(x) = \sum_{i=0}^{n} y_i \prod_{j \neq i} \frac{x - x_j}{x_i - x_j}
   ```

## Legkisebb négyzetek módszere

A legkisebb négyzetek módszere egy adatfüggvény közelítésére szolgál úgy, hogy minimalizálja az adatok és a közelítő függvény közötti négyzetes eltérések összegét.

1. **Lineáris legkisebb négyzetek**: Egy egyenes illesztése az adatokhoz.

   ```math
   y = mx + b
   ```

2. **Nemlineáris legkisebb négyzetek**: Egy komplexebb függvény illesztése az adatokhoz.

A numerikus módszerek alkalmazása lehetővé teszi a komplex matematikai problémák megoldását közelítő megoldásokkal, amelyeket számítógépes számítások során hatékonyan alkalmazhatunk.