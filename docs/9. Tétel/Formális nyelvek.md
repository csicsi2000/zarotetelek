# Formális nyelvek

## Ábécék, szavak, formális nyelvek

- **Ábécé**: Egy véges halmaz, amely tartalmazza az összes lehetséges szimbólumot vagy karaktert, amelyeket egy adott nyelvben használnak.
- **Szavak**: Olyan sorozatok, amelyeket az ábécé szimbólumaiból alkotnak.
- **Formális nyelvek**: Az ábécé feletti véges vagy végtelen halmazok, amelyek szabályok alapján definiálva vannak.

## Műveletek szavakkal és nyelvekkel

- **Szókonkatenáció**: Két szó összefűzése.
- **Kleene lezárt**: Egy nyelv minden lehetséges szókonkatenációját tartalmazza, beleértve a nulla hosszúságú szót is.
- **Unió**: Két nyelv egyesítése.
- **Metszet**: Két nyelv közös elemeinek kiválasztása.
- **Komplementer**: Egy nyelv azon szavainak kiválasztása, amelyek nincsenek egy másik adott nyelvben.

## Szintaxis-leíró eszközök

A szintaxis-leíró eszközök olyan eszközök, amelyekkel formális nyelveket és szintaktikai elemzéseket írhatunk le. Például a Backus-Naur forma (BNF) vagy az Extended Backus-Naur forma (EBNF).

## Generatív grammatikák, Chomsky-féle osztályozás

- **Generatív grammatikák**: Formális rendszerek, amelyek leírják a nyelvek szerkezetét és generálását szabályok segítségével.
- **Chomsky-féle osztályozás**: Az egységes formátumú generatív grammatikák négy osztályba sorolása a legegyszerűbbtől a legbonyolultabbig: 0., 1., 2., és 3. típusú nyelvek.

## Levezetési fák, elemzési stratégiák

- **Levezetési fák**: Fa struktúrák, amelyek reprezentálják a generatív grammatikák által előállított szavak levezetéseit.
- **Elemzési stratégiák**: Módszerek a szintaktikai elemzéshez, például a balról jobbra elemzés (LR), a jobbról balra elemzés (LL), és a fentről lefelé elemzés (top-down).

## A véges és a verem-automaták, a Turing gépek és változataik ismertetése

- **Véges automaták**: Olyan absztrakt modellek, amelyek véges számú állapotból, átmeneti függvényekből és elfogadó állapotokból állnak.
- **Verem-automaták**: Véges automaták kiegészítve egy verem adatszerkezettel, amelyet az átmeneti függvények módosíthatnak.
- **Turing gépek**: A számításelmélet alapvető modellje, amely véges szalagokból, olvasó-író fejekből és átmeneti függvényekből áll.

## A delta leképezés tulajdonságai, megadási módjai a különböző automaták esetén

- **Delta leképezés**: Az átmeneti függvényeket gyakran delta (Δ) leképezésekkel reprezentálják. Ezek meghatározzák, hogy egy adott állapotból egy adott bemenet esetén melyik állapotba és verembe kell átlépni.
- **Véges automaták esetén**: A delta leképezése véges számú állapot közötti átmenetekkel és bemenetekkel.
- **Verem-automaták esetén**: A delta leképezése állapotok és bemenetek mellett verem műveleteket is tartalmazhat.
- **Turing gépek esetén**: A delta leképezése állapotok, olvasott szimbólumok, írási műveletek és fejmozgások számára.

## Az automaták és a grammatikák kapcsolata

Az automaták és a generatív grammatikák között szoros kapcsolat van. Az automaták leírják a nyelvek formális struktúráját és elfogadási mechanizmusát, míg a generatív grammatikák a nyelvek generálását írják le. A Chomsky-féle osztályozás egyik fontos vonatkozása éppen az, hogy az egyes osztályokhoz milyen típusú nyelvek tartoznak, és melyik típusú generatív grammatika írható le az adott nyelvhez.