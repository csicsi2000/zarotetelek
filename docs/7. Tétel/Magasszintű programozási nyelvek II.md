# Magasszintű programozási nyelvek II

## Öröklődés

Az öröklődés olyan mechanizmus, amely lehetővé teszi az osztályoknak, hogy örököljenek tulajdonságokat és viselkedéseket egy másik osztályból, ami lehetővé teszi a kód újrafelhasználását és a hierarchiák létrehozását.

## Korai kötés, késői kötés

### Korai kötés (Early Binding)

A korai kötés azt jelenti, hogy a fordítási időben történik a változók, függvények és osztályok kapcsolódása. Ez az információ már a fordítás során ismert, és így gyorsabb végrehajtást eredményezhet, de kevésbé rugalmas, mivel a típusokat előre kell ismerni.

### Késői kötés (Late Binding)

A késői kötés azt jelenti, hogy a kapcsolatok csak futási időben kerülnek meghatározásra. Ezáltal a program rugalmasabb lesz, mivel dinamikusan kezelhetők az objektumok és az interfészek, de ez gyakran lassabb futási időt eredményez.

## Konstruktorok, konstruktorhívási lánc, osztályszintű konstruktor

### Konstruktorok

A konstruktor egy speciális metódus az osztályban, amelyet a példány létrehozásakor hívunk meg. A konstruktor felelős az osztály inicializálásáért és az objektum állapotának beállításáért.

### Konstruktorhívási lánc

Ha egy osztály örökli egy másik osztályt, akkor a szülőosztály konstruktorát is meg kell hívni a leszármazott osztály konstruktorának a részeként. Ez a konstruktorhívási lánc segítségével történik, amely általában a leszármazott osztály konstruktorának első lépése.

### Osztályszintű konstruktor

Az osztályszintű konstruktor egy speciális konstruktor, amelyet csak egyszer hívnak meg, amikor az osztály először példányosítódik vagy hozzáférnek az osztály statikus tagjaihoz. Ezt a konstruktort gyakran használják az osztályon belüli statikus inicializációhoz.

## Típuskompatibilitás, object osztály

### Típuskompatibilitás

A típuskompatibilitás azt jelenti, hogy egy adott típusú objektumot hogyan lehet kezelni egy másik típusú objektumként. Például egy leszármazott osztály objektumát gyakran úgy lehet kezelni, mint a szülőosztály objektumát, mivel a leszármazott osztály örökli a szülőosztály tulajdonságait és viselkedését.

### Object osztály

Az Object osztály az összes Java osztály alapja, mivel az összes osztály közvetlenül vagy közvetve örökli ezt az osztályt. Az Object osztály rendelkezik néhány alapvető metódussal, például toString(), equals(), hashCode(), ami minden osztályban felülírható.

## Lepecsételt osztályok és statikus osztályok

### Lepecsételt osztályok (Sealed Classes)

A lepecsételt osztályok olyan osztályok, amelyek csak a meghatározott osztályokból származhatnak. Ez lehetővé teszi a programozók számára, hogy meghatározzák az adatok típusát és struktúráját, és biztosítsák, hogy csak a megengedett típusokat használják.

### Statikus osztályok (Static Classes)

A statikus osztályok olyan osztályok, amelyek nem példányosíthatók, és csak statikus tagokat tartalmazhatnak, például statikus metódusokat vagy statikus tulajdonságokat. Ezek hasznosak, ha egy osztálynak nincs szüksége példányosításra, és csak egy adott kontextusban használják az osztály funkcióit.

A magasszintű programozási nyelvekben az öröklődés, a konstruktorok és a típuskompatibilitás fontos koncepciók, amelyek lehetővé teszik a kód strukturális szervezését és az objektumorientált programozás előnyeinek kiaknázását. A különböző kötési mechanizmusok és az osztályok speciális típusai további rugalmasságot és funkcionalitást biztosítanak a programozáshoz.