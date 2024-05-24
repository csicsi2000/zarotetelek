# Adatbázisrendszerek I.

## Hierarchikus, hálós és relációs modellek

### Hierarchikus modell

A hierarchikus adatmodell egy fa alapú struktúra, ahol az adatok hierarchikus kapcsolatban állnak egymással. Minden egyes rekordnak pontosan egy szülője és több gyermeke lehet.

- **Előnyök**: 
  - Egyszerű adatkapcsolatok.
  - Gyors adatkeresés a hierarchia mentén.

- **Hátrányok**: 
  - Nehézkes a bonyolult kapcsolatok kezelése.
  - Szülő-gyermek kapcsolatok merevsége.

### Hálós modell

A hálós adatmodell egy gráf alapú struktúra, ahol az adatok rugalmasabb kapcsolatban állnak egymással, mint a hierarchikus modellben. Egy rekordnak több szülője és több gyermeke is lehet.

- **Előnyök**:
  - Rugalmasabb adatszerkezet.
  - Bonyolultabb kapcsolatok kezelése.

- **Hátrányok**:
  - Bonyolultabb adatkezelés.
  - Összetettebb adatbázis-karbantartás.

### Relációs modell

A relációs adatmodell táblák formájában tárolja az adatokat, ahol minden tábla sorokból és oszlopokból áll. A táblák közötti kapcsolatokat kulcsok segítségével kezelik.

- **Előnyök**:
  - Egyszerűsített adatstruktúra.
  - Könnyű adatkezelés SQL segítségével.
  - Rugalmas adatkapcsolatok.

- **Hátrányok**:
  - Teljesítményproblémák nagy adatmennyiség esetén.
  - Bonyolultabb adattervezés.

## Kulcsok a relációs modellben

### Elsődleges kulcs (Primary Key)

Az elsődleges kulcs egy vagy több attribútumból áll, amelyek egyértelműen azonosítanak egy rekordot a táblában. 

### Idegen kulcs (Foreign Key)

Az idegen kulcs egy vagy több attribútumból áll, amelyek egy másik tábla elsődleges kulcsára hivatkoznak, ezzel kapcsolatot hozva létre a két tábla között.

### Egyedi kulcs (Unique Key)

Az egyedi kulcs biztosítja, hogy az adott attribútum(ok) értékei egyediek legyenek a táblán belül, de nem szolgál elsődleges kulcsként.

## Kapcsolatok

### Egy-egy típusú kapcsolat (One-to-One)

Egy rekord az egyik táblában pontosan egy rekordhoz kapcsolódik egy másik táblában.

### Egy-sok típusú kapcsolat (One-to-Many)

Egy rekord az egyik táblában több rekordhoz is kapcsolódhat egy másik táblában.

### Sok-sok típusú kapcsolat (Many-to-Many)

Több rekord az egyik táblában több rekordhoz kapcsolódhat egy másik táblában. Általában egy köztes tábla segítségével valósítják meg.

## Anomáliák

### Beszúrási anomália (Insertion Anomaly)

Olyan probléma, amikor az új adatok beszúrása miatt redundáns adatokat kell felvenni vagy bizonyos adatokat nem lehet beszúrni.

### Törlési anomália (Deletion Anomaly)

Olyan probléma, amikor egy adat törlése miatt más, fontos adatok is elvesznek.

### Módosítási anomália (Update Anomaly)

Olyan probléma, amikor egy adat módosítása miatt több helyen is módosítani kell az adatbázisban, ami redundanciához vezet.

## Funkcionális függőségek

A funkcionális függőség azt jelenti, hogy egy attribútum (vagy attribútumok halmaza) egyértelműen meghatároz egy másik attribútumot (vagy attribútumok halmazát). 

- **Jelölés**: \( A \rightarrow B \) azt jelenti, hogy az A attribútumból következik a B attribútum.

## Tranzitivitás

A tranzitivitás egy speciális funkcionális függőség, ahol ha \( A \rightarrow B \) és \( B \rightarrow C \) fennáll, akkor \( A \rightarrow C \) is fennáll.

## Normálformák

A normálformák célja az adatbázis redundanciájának csökkentése és az anomáliák elkerülése. A leggyakoribb normálformák:

### Első normálforma (1NF)

Egy tábla akkor van első normálformában, ha minden attribútuma atomi értéket tartalmaz, és minden rekord egyedi.

### Második normálforma (2NF)

Egy tábla akkor van második normálformában, ha első normálformában van, és minden nem kulcs attribútuma teljes függőséget mutat az elsődleges kulcs minden részhalmazával szemben.

### Harmadik normálforma (3NF)

Egy tábla akkor van harmadik normálformában, ha második normálformában van, és nincs tranzitív függőség a nem kulcs attribútumok között.

### Boyce-Codd normálforma (BCNF)

Egy tábla akkor van Boyce-Codd normálformában, ha harmadik normálformában van, és minden determináns szuperkulcs.