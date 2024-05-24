# Adatbázisrendszerek II.: A PL/SQL alapjai

## Típusok, változók, konstansok, vezérlési szerkezetek

- **Típusok**: A PL/SQL-ben lehetőség van saját adattípusok létrehozására, például rekordok, tömbök vagy tábla típusok.
- **Változók**: A változók tárolják az adatokat a PL/SQL programokban, és deklaráció után használhatók.
- **Konstansok**: Állandó értékeket tárolnak, amelyek nem változnak futásidő alatt.
- **Vezérlési szerkezetek**: A vezérlési szerkezetek segítségével a program vezérlését, mint például a ciklusokat vagy elágazásokat, szabályozhatjuk.

## SQL utasítások elhelyezésének és használatának lehetőségei a PL/SQL-ben

- A PL/SQL-ben SQL utasításokat közvetlenül elhelyezhetünk a kódban, vagy külön SQL blokkokban is futtathatjuk azokat.
- A SQL utasításokat cursorok segítségével is használhatjuk a PL/SQL-ben eredményhalmazok feldolgozására.

## A PL/SQL program felépítése

- Egy PL/SQL program többnyire blokkokból áll, amelyeknek van egy kezdő és egy végző része.
- A blokkokban lehetnek változók, utasítások és vezérlési szerkezetek.

## Blokkok és alprogramok

- **Blokkok**: A PL/SQL programok alapegységei, amelyekben utasítások hajthatók végre.
- **Alprogramok**: Újrafelhasználható kódrészletek, amelyek önállóan is futtathatók, és paramétereket fogadhatnak.

## Tárolt eljárások, tárolt függvények összehasonlítása, csomagok készítésének célja és lehetőségei

- **Tárolt eljárások**: PL/SQL blokkok, amelyekben adatmanipulációs vagy egyéb feladatok hajthatók végre.
- **Tárolt függvények**: Visszatérő értékkel rendelkező PL/SQL blokkok.
- **Csomagok**: A csomagok összefogják a tárolt eljárásokat és függvényeket, valamint más típusdefiníciókat és globális változókat egy egységes egységben.

## A tárolt alprogramok paraméterezési lehetőségei, az egyes lehetőségek jellemzői

- A tárolt eljárások és függvények paramétereket fogadhatnak, amelyek lehetnek bemenő, kimenő vagy mindkettő egyidejűleg.
- A paraméterek lehetnek kötelezőek vagy opcionálisak, valamint pozíció szerinti vagy név szerinti megadással használhatók.

## Kivételek kezelés PL/SQL-ben

- A kivételek a PL/SQL-ben hibák vagy különleges esetek kezelésére szolgálnak.
- A kivételeket a `EXCEPTION` blokkban lehet kezelni a program szétesése nélkül.
- A `RAISE` utasítással kivételeket dobhatunk, és a `EXCEPTION WHEN` szerkezettel kezelhetjük azokat.