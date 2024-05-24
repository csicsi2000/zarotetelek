# Webprogramozás II.

## Dinamikus weboldalak jellemzői és összehasonlításuk a statikus tartalmakkal

- **Dinamikus weboldalak**: Olyan weboldalak, amelyek tartalma dinamikusan változik a felhasználó interakciója vagy más változók hatására.
- **Statikus tartalmak**: Olyan weboldalak, amelyek tartalma előre elkészített és nem változik dinamikusan.

## A PHP nyelv jellemzői és használatának feltételei a webfejlesztés során

- **PHP**: Egy szkriptnyelv, amelyet főként webfejlesztésre használnak.
- **Használat feltételei**: A PHP futtatásához szükség van egy szerverre, amely támogatja a PHP-t, például Apache vagy Nginx. A PHP fájlokat a szerver oldalon kell futtatni.

## Kliens és szerver oldali infrastruktúra a PHP futtatásához

- **Kliensoldal**: A felhasználó böngészőjében futó kód, amely HTML, CSS és JavaScript-tartalmakat tartalmaz.
- **Szerveroldal**: A szerveren futó kód, például a PHP, amely generálja a dinamikus tartalmat a felhasználó kérésére.

## A PHP típusrendszere: típusok, konstansok, változók a PHP-ban

- **Típusok**: A PHP változói lehetnek egyszerű típusok (pl. egész számok, lebegőpontos számok, karakterláncok) vagy összetett típusok (pl. tömbök, objektumok).
- **Konstansok**: Olyan értékek, amelyek nem változnak futás közben.
- **Változók**: Olyan tárolók, amelyek értéke változhat futás közben.

## A HTML és a PHP kapcsolata

- A PHP lehetővé teszi a dinamikus tartalom generálását HTML oldalakon keresztül. A PHP kód beágyazható a HTML-be, és dinamikusan generálhatja az HTML tartalmat.

## Modulszerkezet kialakítása, a forráskód újrahasznosításának lehetőségei

- Az újrahasznosítható kódokat el kell különíteni modulokba, amelyek könnyen újrahasználhatók más részekben vagy más projektekben.
- A PHP lehetővé teszi az include és require utasítások használatát, amelyekkel más PHP fájlok tartalmát lehet beilleszteni az aktuális fájlba.

## Adatcsere a kliens és szerver oldal között

- Az adatcsere a kliens és a szerver között általában HTTP kérések és válaszok formájában történik.
- A kliens oldal JavaScript segítségével küldhet AJAX kéréseket a szervernek, amelyek aszinkron módon adatokat cserélnek.

## Biztonsági kérdések

- Fontos biztonsági szempontokat figyelembe venni a PHP alkalmazások fejlesztése során, például a SQL injekció vagy a cross-site scripting (XSS) elleni védekezés.
- A biztonságos kódolási gyakorlatok, például a változók megfelelő ellenőrzése és a bemenet validálása kulcsfontosságú.

## Munkafolyamatok és sütik kezelése

- A munkafolyamatokat PHP segítségével lehet kezelni, például a session-ök létrehozásával és kezelésével.
- A sütiket (cookies) a felhasználó számítógépén tárolt kis adatfájlok segítségével lehet kezelni, amelyeket a szerver a böngészőnek küld. A sütik lehetővé teszik a felhasználó azonosítását vagy az oldal beállításainak megjegyzését.