# Operációs rendszerek

## Az operációs rendszer fogalmai

### Operációs rendszer (OS)

Az operációs rendszer egy olyan szoftver, amely kezeli a hardver erőforrásokat, és szolgáltatásokat nyújt a számítógépes programok számára. Főbb feladatai közé tartozik a processzkezelés, memória menedzsment, fájlkezelés, és eszközkezelés.

### Kernel

A kernel az operációs rendszer magja, amely közvetlenül kommunikál a hardverrel, és végrehajtja a legalapvetőbb feladatokat, mint például a memóriakezelés, processz ütemezés és eszközkezelés.

### Processz

A processz egy futó program példánya, amely saját memóriaterülettel és erőforrásokkal rendelkezik. A processzeket az operációs rendszer kezeli és ütemezi.

## Virtualizáció

A virtualizáció egy technológia, amely lehetővé teszi, hogy egy fizikai gépen több virtuális gép fusson, mindegyik saját operációs rendszerrel és alkalmazásokkal. Ez növeli a hardver kihasználtságát és rugalmasságát.

## Az operációs rendszerek fájl- és könyvtárkezelése

### Fájlrendszerek

A fájlrendszerek strukturált módon tárolják az adatokat egy tárolóeszközön. Példák különböző fájlrendszerekre: NTFS, FAT32, ext4, HFS+.

### Fájl- és könyvtárkezelés

Az operációs rendszerek különböző módszereket biztosítanak a fájlok és könyvtárak kezelésére, mint például a létrehozás, másolás, törlés és áthelyezés.

## Diszk kezelés, RAID tömbök

### Diszk kezelés

A diszk kezelés az operációs rendszer azon képessége, hogy kezelje a merevlemezek és SSD-k partícióit és formázását. Ide tartozik a lemezterület kiosztása és a fájlrendszer karbantartása.

### RAID tömbök

A RAID (Redundant Array of Independent Disks) technológia több merevlemezt egyesít egyetlen logikai egységgé a teljesítmény növelése vagy az adatbiztonság érdekében. RAID szintek például: RAID 0, RAID 1, RAID 5, RAID 10.

## Átirányítások és szűrők

### Átirányítások

Az átirányítások segítségével a parancsok bemenetét és kimenetét lehet irányítani. Például a kimenet átirányítása egy fájlba:

```bash
ls > list.txt
```

### Szűrők

A szűrők olyan parancsok, amelyek bemenetként adatokat kapnak, feldolgozzák azokat, és az eredményt kimenetként adják vissza. Például a `grep` szűrő:

```bash
grep "keyword" file.txt
```

## Jogosultsági rendszerek

### Működés

A jogosultsági rendszerek szabályozzák, hogy mely felhasználók és csoportok milyen műveleteket végezhetnek fájlokon és könyvtárakon.

### Azonosságok és különbségek az egyes rendszerekben

- **Unix/Linux**: Felhasználók, csoportok, és hozzáférési jogok (rwx) fájlokra és könyvtárakra.
- **Windows**: NTFS jogosultságok, amelyeket ACL-ek (Access Control List) szabályoznak.

## Processz kezelés

A processz kezelés az operációs rendszer azon képessége, hogy létrehozza, ütemezi és kezeli a processzeket. Ide tartozik a többprocesszoros rendszerek támogatása és a különböző ütemezési algoritmusok alkalmazása.

## Szignálok és kezelésük

A szignálok aszinkron események, amelyeket az operációs rendszer küld a processzeknek, hogy különböző eseményekről tájékoztassa őket. Például:

- **SIGINT**: A felhasználó megszakította a programot (Ctrl+C).
- **SIGKILL**: A processz azonnali befejezése.

A szignálokat a processzek kezelhetik saját szignálkezelő függvényekkel.

## Adatmentés és archiválás módszerei és eszközei

### Adatmentés

Az adatmentés célja, hogy biztonsági másolatot készítsünk a fontos adatokról, hogy azokat egy adatvesztés esetén visszaállíthassuk. Példák:

- **Teljes mentés**: Az összes adat mentése.
- **Inkrementális mentés**: Csak a legutóbbi mentés óta megváltozott adatok mentése.
- **Differenciális mentés**: Az utolsó teljes mentés óta megváltozott adatok mentése.

### Archiválás

Az archiválás hosszú távú adatmegőrzést jelent, gyakran történelmi adatok tárolására használják. Példák eszközökre:

- **Tar**: Fájlok és könyvtárak csoportosítása egyetlen fájlba.
- **Zip**: Tömörítés és archiválás.

## Shell-scriptek

A shell-scriptek parancsok sorozata, amelyeket egy shell környezetben futtatnak. Ezek automatizálhatják a rendszeradminisztrációs feladatokat és más ismétlődő műveleteket. Példa egy egyszerű shell-scriptre:

```bash
#!/bin/bash
echo "Hello, World!"
```

Shell-scriptek írása és futtatása lehetővé teszi a rendszerek hatékonyabb kezelését és az automatizálás növelését.