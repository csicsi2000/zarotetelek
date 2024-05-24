# Adatbázisrendszerek II.

## Kurzorok

- **Implicit kurzorok**: Automatikusan létrejönnek, amikor egy SQL lekérdezést végrehajtanak a PL/SQL-ben.
- **Explicit kurzorok**: Kézzel kell létrehozni őket a PL/SQL kódban, és explicit módon kell vezérelni őket.

## Kurzorattribútumok

- A kurzorattribútumok olyan speciális változók, amelyek a kurzor állapotát és a kurzor által visszaadott sorok tulajdonságait tárolják.
- Például a `%FOUND`, `%NOTFOUND`, `%ROWCOUNT` attribútumok segítenek ellenőrizni a kurzor működését és a visszaadott sorok számát.

## Tranzakciókezelés, triggerek a PL/SQL nyelvben

- **Tranzakciókezelés**: A tranzakciók csoportokban hajtanak végre adatbázis-műveleteket, és biztosítják a konzisztenciát és az adatintegritást.
- **Triggerek**: A triggerek speciális PL/SQL eljárások, amelyek automatikusan futnak, amikor meghatározott események történnek az adatbázisban, például INSERT, UPDATE vagy DELETE műveletek.

## Összetett adatszerkezetek (kollekciók) típusai, jellemzői, használatának lehetőségei és előnyei, hátrányai

- **Típusok**: Tömbök (VARRAY), asszociatív tömbök (PL/SQL táblák), gyűjtemények (Nested Tables).
- **Jellemzők**: Rugalmas méret, több dimenziós lehetőség, gyors adatelérést biztosítanak.
- **Használat lehetőségei**: Adatok tárolása és manipulálása nagyobb csoportokban, összetettebb adatmodellek kezelése.
- **Előnyök**: Gyors adatelérés, könnyű használat, lehetőség az adatok csoportosítására és kezelésére.
- **Hátrányok**: Kevésbé hatékony nagy adatmennyiségek esetén, a komplexitás növekedése.