# Architektúrák

## A cache használata

A cache egy kisebb, gyorsabb memória, amely a gyakran használt adatok ideiglenes tárolására szolgál, hogy csökkentse az átlagos hozzáférési időt a főmemóriához képest. A cache használatának célja a teljesítmény növelése azáltal, hogy a processzor gyorsabban hozzáférhet a gyakran használt adatokhoz és utasításokhoz.

## Lokalitási elvek ismertetése

A lokalitás elve két fő koncepciót foglal magában:

1. **Időbeli lokalitás (Temporal Locality)**: Ha egy adatot vagy utasítást nemrégiben használtak, akkor valószínűleg hamarosan újra használni fogják.
   
2. **Térbeli lokalitás (Spatial Locality)**: Ha egy adatot vagy utasítást nemrégiben használtak, akkor valószínűleg a közelében lévő adatokat vagy utasításokat is hamarosan használni fogják.

Ezek az elvek segítik a cache hatékonyságának növelését, mivel a cache gyakran használt adatokat és azok környezetét tartja.

## A memória hierarchia szintjeinek összehasonlítása

A memória hierarchia különböző szintekből áll, amelyek különböző sebességgel és kapacitással rendelkeznek:

1. **Regiszterek**: Nagyon gyors, közvetlenül a processzorban található, nagyon korlátozott kapacitás.
2. **Cache memória**:
   - **L1 Cache**: Leggyorsabb, legközelebb a processzorhoz, de a legkisebb kapacitású.
   - **L2 Cache**: Kicsit lassabb, nagyobb kapacitású.
   - **L3 Cache**: Még lassabb, de még nagyobb kapacitású, általában több mag osztozik rajta.
3. **Főmemória (RAM)**: Nagy kapacitású, de lassabb hozzáférési idő.
4. **Másodlagos tároló (SSD/HDD)**: Nagyon nagy kapacitású, de lassú hozzáférési idő.

## A cache helye a memória hierarchiában

A cache a regiszterek és a főmemória között helyezkedik el a memória hierarchiában. Az L1 cache a legközelebb van a processzorhoz, míg az L2 és L3 cache-ek távolabb helyezkednek el, de még mindig gyorsabbak, mint a főmemória.

## A cache felépítése, az elérési változatok

### Cache felépítése

A cache memória blokkokra (cache lines) van osztva, és minden blokk több adatot tartalmaz. A cache általában több szintből áll (L1, L2, L3), amelyek különböző méretűek és sebességűek.

### Elérési változatok

1. **Direct-mapped cache**: Minden memóriacím egyetlen lehetséges helyre kerülhet a cache-ben.
   
2. **Fully associative cache**: Bármely memóriacím bármelyik helyre kerülhet a cache-ben.

3. **Set-associative cache**: A cache több készletre van osztva, és minden készletben több hely van. Minden memóriacím egy adott készletbe kerülhet, de a készleten belül bármelyik helyre.

## Címbitek számának meghatározása az elérési módoktól függően

A cache címzése több részből áll:

1. **Tag**: Azonosítja a memóriablokkot a cache-ben.
2. **Index**: Azonosítja a készletet a set-associative cache-ben.
3. **Offset**: Azonosítja a pontos helyet a cache sorban (line).

### Direct-mapped cache címzés

- **Tag**: Maradék címrész, miután az index és az offset levonásra került.
- **Index**: Azonosítja a sorokat a cache-ben.
- **Offset**: Azonosítja a pontos helyet a sorban.

### Fully associative cache címzés

- **Tag**: Az egész cím, kivéve az offsetet.
- **Offset**: Azonosítja a pontos helyet a sorban.

### Set-associative cache címzés

- **Tag**: Azonosítja a memóriablokkot a készleten belül.
- **Index**: Azonosítja a készletet a cache-ben.
- **Offset**: Azonosítja a pontos helyet a sorban.

## Visszaírási módok

### Write-through

Az adatok azonnal a főmemóriába kerülnek írásra a cache-be történő íráskor. Ez biztosítja, hogy a főmemória mindig naprakész, de növelheti a memóriahozzáférési időt.

### Write-back

Az adatok először a cache-be kerülnek írásra, és csak akkor kerülnek a főmemóriába, amikor a cache vonalat ki kell cserélni. Ez csökkenti a memóriahozzáférési időt, de bonyolultabb szinkronizációt igényel.

## A dirty és valid flag-ek szerepe

### Valid flag

A valid flag azt jelzi, hogy a cache vonal érvényes adatokat tartalmaz-e. Ha a valid flag false, akkor a cache vonal nem tartalmaz érvényes adatokat, és nem használható.

### Dirty flag

A dirty flag azt jelzi, hogy a cache vonal módosult-e a főmemóriához képest. Ha a dirty flag true, akkor a cache vonal adatokat tartalmaz, amelyeket vissza kell írni a főmemóriába, mielőtt a cache vonalat felülírják.

A cache használatának és kezelésének megértése kritikus fontosságú a számítógépes rendszerek teljesítményének optimalizálásában. A lokalitási elvek, a memória hierarchia, és a cache felépítése és működése mind hozzájárulnak a hatékony memóriahozzáféréshez és az összesített rendszersebesség növeléséhez.