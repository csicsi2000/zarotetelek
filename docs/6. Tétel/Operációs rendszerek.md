# Operációs rendszerek

## Az operációs rendszerek funkciói, alapfogalmai

### Alapfogalmak

1. **Operációs rendszer (OS)**: Egy szoftver, amely kezeli a számítógépes hardver erőforrásait, és szolgáltatásokat nyújt a számítógépes programok számára.
2. **Kernel**: Az operációs rendszer központi része, amely közvetlenül kommunikál a hardverrel és kezeli az alapvető rendszerfunkciókat.
3. **Processz**: Egy futó program példánya, amely tartalmazza a programkódot és annak végrehajtási állapotát.

### Funkciók

1. **Erőforráskezelés**: A CPU, memória, I/O eszközök és tárolók hatékony kiosztása és kezelése.
2. **Folyamatkezelés**: A processzek létrehozása, ütemezése, szinkronizálása és megszüntetése.
3. **Memóriakezelés**: A memória kiosztása, védelme és felügyelete.
4. **Fájlrendszerkezelés**: A fájlok és könyvtárak szervezése, tárolása, keresése és kezelése.
5. **Biztonság és jogosultságkezelés**: A rendszer erőforrásaihoz való hozzáférés szabályozása és védelme.

## A virtualizáció

### Fogalma

A virtualizáció a hardveres erőforrások absztrakcióját jelenti, amely lehetővé teszi, hogy egy fizikai gépen több virtuális gép (VM) fusson, mindegyik saját operációs rendszerrel és alkalmazásokkal.

### Típusai

1. **Teljes virtualizáció**: A virtuális gép teljes mértékben emulálja a hardvert, lehetővé téve a vendég operációs rendszer teljes izolációját.
2. **Paravirtualizáció**: A vendég operációs rendszer tudatában van, hogy egy virtuális környezetben fut, és optimalizált hívásokat használ a hatékonyabb működés érdekében.
3. **Konténerizáció**: Az operációs rendszer szintjén történő virtualizáció, ahol az alkalmazások és azok függőségei izolált konténerekben futnak.

## Processz kezelés

### Folyamatok létrehozása és megszüntetése

1. **Létrehozás**: Új folyamatokat hoz létre egy program végrehajtásához.
2. **Megszüntetés**: Folyamatok befejezése, amikor a végrehajtásuk véget ér, vagy erőforrások felszabadítása.

### Ütemezés

Az operációs rendszer döntései a processzek futtatási sorrendjéről és CPU-hozzáférésük kiosztásáról. Az ütemezési algoritmusok közé tartoznak a First-Come, First-Served (FCFS), Round Robin (RR), és Priority Scheduling.

### Szinkronizáció és kommunikáció

Folyamatok közötti adatcserére és együttműködésre szolgáló mechanizmusok, például semaforok, mutexek, üzenetsorok és csatornák.

## Fájlrendszerek és szolgáltatásaik

### Fájlrendszerek

A fájlrendszerek a fájlok és könyvtárak szervezésének módjai, példák: FAT, NTFS, ext3, ext4.

### Szolgáltatások

1. **Fájlok létrehozása és törlése**: Új fájlok és könyvtárak létrehozása, valamint meglévők törlése.
2. **Olvasás és írás**: Fájlok tartalmának olvasása és módosítása.
3. **Keresés**: Fájlok és könyvtárak keresése és elérése a fájlrendszerben.
4. **Hozzáférés védelem**: Jogosultságok beállítása és ellenőrzése a fájlokhoz és könyvtárakhoz való hozzáférés szabályozására.

## Hibatűrő diszk rendszerek

### RAID rendszerek

RAID (Redundant Array of Independent Disks) technológia a hibatűrő és nagy teljesítményű tárolórendszerek kialakítására. 

1. **RAID 0**: Szalagos elrendezés, nincs hibatűrés, csak teljesítmény növelés.
2. **RAID 1**: Tükrözés, adatok másolása két lemezre, magas hibatűrés.
3. **RAID 5**: Szalagos elrendezés paritással, adatvédelem és teljesítmény egyensúlya.
4. **RAID 6**: Szalagos elrendezés dupla paritással, magasabb hibatűrés.

### Hibatűrés és helyreállítás

A diszk rendszerek hibáinak és adatvesztésének elkerülésére, valamint helyreállítására szolgáló technikák, például tartalék diszkek használata, paritás információk és tükrözés.

## Jogosultsági rendszerek az operációs rendszerekben

### Működés

Az operációs rendszerek jogosultsági rendszerei szabályozzák, hogy mely felhasználók és folyamatok milyen műveleteket végezhetnek a rendszer erőforrásain. Ez magában foglalja a fájlokhoz, könyvtárakhoz, memóriaterületekhez és hardveres eszközökhöz való hozzáférés szabályozását.

### Azonosítás és hitelesítés

1. **Azonosítás (Identification)**: A felhasználók és folyamatok egyedi azonosítása, például felhasználónév vagy azonosító (ID) alapján.
2. **Hitelesítés (Authentication)**: A felhasználók és folyamatok személyazonosságának ellenőrzése, például jelszó, biometrikus adatok vagy kétfaktoros hitelesítés segítségével.

### Hozzáférés-vezérlés

1. **Hozzáférési listák (ACL)**: Részletes hozzáférési szabályok meghatározása minden erőforráshoz, felsorolva, hogy ki mit tehet az adott erőforrással.
2. **Szerepköralapú hozzáférés-vezérlés (RBAC)**: A felhasználók különböző szerepkörökhöz való hozzárendelése, és a szerepkörök jogainak meghatározása.

Az operációs rendszerek alapvető funkcióinak, folyamatainak és szolgáltatásainak megértése elengedhetetlen a számítógépes rendszerek hatékony és biztonságos használatához. A virtualizáció és a hibatűrő rendszerek használata lehetővé teszi a nagyobb megbízhatóságot és rugalmasságot, míg a jogosultsági rendszerek biztosítják az erőforrások megfelelő védelmét és kezelését.