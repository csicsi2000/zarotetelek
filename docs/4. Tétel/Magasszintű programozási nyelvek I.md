# Magasszintű programozási nyelvek I

## Alaptípusok, változók, konstansok, literálok

### Alaptípusok

Az alaptípusok azok a legegyszerűbb adattípusok, amelyeket a programozási nyelvek biztosítanak. Ezek közé tartoznak:

- **Egész számok (Integer)**: pl. `int` típus
- **Valós számok (Floating-point)**: pl. `float`, `double` típus
- **Logikai értékek (Boolean)**: pl. `bool` típus
- **Karakterek (Character)**: pl. `char` típus
- **Szövegek (String)**: pl. `string` típus

### Változók

A változók olyan névvel ellátott memóriaterületek, amelyek értéket tárolnak, és amelyeket a program futása során módosíthatunk.

```python
int a = 5;
float b = 3.14;
```

### Konstansok

A konstansok olyan névvel ellátott memóriaterületek, amelyek értéke a program futása során nem változtatható meg.

```python
const int MAX_VALUE = 100;
```

### Literálok

A literálok közvetlenül az értékeket képviselik a kódban.

```python
42        // egész szám literál
3.14      // valós szám literál
'c'       // karakter literál
"hello"   // szöveg literál
true      // logikai literál
```

## Operátorok

Az operátorok olyan speciális szimbólumok, amelyekkel műveleteket végezhetünk az operandusokon.

### Aritmetikai operátorok

- **Összeadás (+)**: `a + b`
- **Kivonás (-)**: `a - b`
- **Szorzás (*)**: `a * b`
- **Osztás (/)**: `a / b`
- **Maradékos osztás (%)**: `a % b`

### Relációs operátorok

- **Egyenlő (==)**: `a == b`
- **Nem egyenlő (!=)**: `a != b`
- **Kisebb (<)**: `a < b`
- **Nagyobb (>)**: `a > b`
- **Kisebb vagy egyenlő (<=)**: `a <= b`
- **Nagyobb vagy egyenlő (>=)**: `a >= b`

### Logikai operátorok

- **És (&&)**: `a && b`
- **Vagy (||)**: `a || b`
- **Negáció (!) **: `!a`

### Bitműveleti operátorok

- **És (&)**: `a & b`
- **Vagy (|)**: `a | b`
- **Exkluzív vagy (^)**: `a ^ b`
- **Balra tolás (<<)**: `a << 1`
- **Jobbra tolás (>>)**: `a >> 1`

## Szelekciós vezérlési szerkezetek

A szelekciós vezérlési szerkezetek lehetővé teszik a program számára, hogy különböző utasításokat hajtson végre attól függően, hogy egy feltétel igaz vagy hamis.

### If-else szerkezet

```python
if (feltétel) {
    // kódblokk, ha a feltétel igaz
} else {
    // kódblokk, ha a feltétel hamis
}
```

### Switch szerkezet

```python
switch (kifejezés) {
    case érték1:
        // kódblokk
        break;
    case érték2:
        // kódblokk
        break;
    default:
        // alapértelmezett kódblokk
}
```

## Ciklusok

A ciklusok lehetővé teszik, hogy egy kódrészlet többször ismétlődjön.

### For ciklus

```python
for (kezdet; feltétel; lépés) {
    // kódblokk
}
```

### While ciklus

```python
while (feltétel) {
    // kódblokk
}
```

### Do-while ciklus

```python
do {
    // kódblokk
} while (feltétel);
```

## Érték- és referenciatípusok memóriamenedzsmentje, stack és heap

### Értéktípusok

Az értéktípusok olyan típusok, amelyek értékei közvetlenül a stack memóriában tárolódnak.

```python
int x = 10;  // x közvetlenül tárolja az értéket
```

### Referenciatípusok

A referenciatípusok olyan típusok, amelyek értékei a heap memóriában tárolódnak, és a stack csak a hivatkozást (referenciát) tartalmazza.

```python
string s = "hello";  // s hivatkozás a heap-en tárolt értékre
```

## Változók hatásköre és élettartama

### Hatáskör (Scope)

A hatáskör azt jelenti, hogy a változó mely részeken elérhető a kódban.

- **Lokális változók**: Csak a deklarációs blokkon belül érhetők el.
- **Globális változók**: Az egész programban elérhetők.

### Élettartam (Lifetime)

A változó élettartama azt jelenti, hogy a változó meddig létezik a memóriában.

- **Statikus változók**: A program teljes futási ideje alatt léteznek.
- **Automatikus változók**: A blokkon belül jönnek létre és megsemmisülnek a blokk végén.

## Programozási nyelvek generációi

### Első generációs nyelvek (1GL)

- Gépi kód, amely közvetlenül a hardveren fut.

### Második generációs nyelvek (2GL)

- Assembly nyelvek, amelyek az ember által olvasható mnemonikus kódokat használják.

### Harmadik generációs nyelvek (3GL)

- Magasszintű nyelvek, mint például C, C++, Java, Python.

### Negyedik generációs nyelvek (4GL)

- Magasabb szintű, domén specifikus nyelvek, mint például SQL, MATLAB.

### Ötödik generációs nyelvek (5GL)

- Problémamegoldó nyelvek, mint például Prolog, amelyek mesterséges intelligencia és logikai programozási megközelítéseket használnak.

## Imperatív és deklaratív nyelvek

### Imperatív nyelvek

Az imperatív nyelvekben a programozó utasításokat ad a számítógépnek, hogy milyen lépéseket hajtson végre a cél elérése érdekében.

- **Példák**: C, C++, Java

### Deklaratív nyelvek

A deklaratív nyelvekben a programozó megadja, hogy mit szeretne elérni, nem pedig azt, hogy hogyan érje el.

- **Példák**: SQL, HTML, Prolog