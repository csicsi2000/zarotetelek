# Bevezetés a számítógépi grafikába

## Raszteres algoritmusok

### DDA és MidPoint szakaszrajzoló algoritmusok

- **DDA (Digital Differential Analyzer)**: Egy egyszerű, lineáris interpolációs algoritmus, amelyet szakaszok rajzolására használnak.
- **MidPoint szakaszrajzoló algoritmus**: A Bresenham algoritmus egyik változata, amely hatékonyan rajzol szakaszokat raszterkijelzőn.

### MidPoint körrajzoló algoritmus

- Egy hatékony algoritmus, amely körök rajzolására szolgál.

### Cohen-Sutherland vágó algoritmus

- Egy algoritmus, amely az adott ablakon kívül eső vonalakat hatékonyan vágja el.

## Paraméteres görbék

### Hermit ív

- Egy paraméteres görbe, amely sima görbét definiál a kezdeti pontjának, végpontjának és a hozzájuk kapcsolódó irányvektoroknak a megadásával.

### Bézier görbe

- Egy másik paraméteres görbe, amelyet vezérlő pontok segítségével definiálnak, és sima görbét hoz létre.

### B-Spline

- Egy rugalmasabb paraméteres görbe, amely megengedi a vezérlő pontok számának és eloszlásának változtatását a görbe simításához.

## Pont-transzformációk síkban, térben, homogén koordináták

- **Síkban**: Transzformációk, amelyek a pontokat síkban mozgatják, elforgatják vagy skálázzák.
- **Térben**: Ugyanezek a transzformációk térbeli pontokon alkalmazva.
- **Homogén koordináták**: Egy kiterjesztett koordináta rendszer, amely lehetővé teszi a transzformációk egyszerűbb kezelését.

## Tér leképezése síkra

### Párhuzamos és centrális vetítés

- **Párhuzamos vetítés**: A tér objektumait párhuzamosan ábrázolja egy síkra.
- **Centrális vetítés**: A tér objektumait egy központi pontra vetíti, amely általában a megfigyelő vagy a kamera pozíciója.

### Axonometria

- Egy speciális módszer a tér objektumainak síkra vetítésére, amely az axonometrikus vetítésre épül.

## Poliéderek megadása

### Wire Frame modell

- Egy egyszerű modellációs technika, amely a poliéder éleit rajzolja ki.

### B-Rep adatstruktúra

- A poliéderek részletes leírását adja meg a csúcsok, élek és lapok összekapcsolásával.

## Poliéderek megjelenítése

### Hátsó lapok eltávolítása

- Egy algoritmus, amely hatékonyan eldobja azokat a hátsó lapokat, amelyek nem láthatóak az adott nézőpontból.

### Z-Buffer algoritmus

- Egy másik algoritmus a hátsó lapok eltávolítására és a mélységi információ tárolására, amely lehetővé teszi a helyes megjelenítést.

## Árnyalás

### Flat-, Gouraud- és Phong árnyalás

- **Flat árnyalás**: Az objektumot egységesen árnyalja, minden pixel ugyanazt a színt kapja.
- **Gouraud árnyalás**: Az objektumot az élei mentén árnyalja, majd interpolálja a színeket a lapokon.
- **Phong árnyalás**: Az objektumot a felület minden pontján árnyalja, és a fényforrásoktól való elhelyezkedését is figyelembe veszi.