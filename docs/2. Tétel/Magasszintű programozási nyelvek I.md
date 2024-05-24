## Magasszintű programozási nyelvek I

### Tömbök és listák

#### Tömbök

**Definíció**: A tömbök azonos típusú elemek fix hosszúságú sorozatai, amelyeket egyetlen név alatt tárolunk. 

**Jellemzők**:
- **Statikus méret**: A tömb méretét a létrehozáskor kell megadni, és az nem változtatható meg.
- **Indexelés**: Az elemek indexelése 0-tól kezdődik.
- **Gyors hozzáférés**: Az elemekhez való hozzáférés konstans időben (\(O(1)\)) történik.

**Példa (C++)**:
```cpp
int arr[5] = {1, 2, 3, 4, 5};
```

**Példa (Python)**:
```python
arr = [1, 2, 3, 4, 5]
```

#### Listák

**Definíció**: A listák dinamikus méretű, tetszőleges típusú elemek sorozatai.

**Jellemzők**:
- **Dinamikus méret**: A lista mérete futás közben változtatható.
- **Könnyű bővítés**: Elemet hozzáadni és eltávolítani egyszerű, de a hozzáférési idő általában lineáris (\(O(n)\)).
- **Nem fix típusú elemek**: A listában különböző típusú elemek is lehetnek.

**Példa (C++)**:
```cpp
#include <vector>
std::vector<int> list = {1, 2, 3, 4, 5};
```

**Példa (Python)**:
```python
list = [1, 2, 3, 4, 5]
```

### Rekordok, class és struct

#### Rekordok

**Definíció**: Rekordok olyan összetett adattípusok, amelyek különböző típusú elemeket (mezőket) tartalmaznak. Általában adatbázisokban használják.

**Példa (Pascal)**:
```pascal
type
  TPerson = record
    Name: string;
    Age: Integer;
  end;
```

#### Class és Struct

**Class (osztály)**

**Definíció**: Az osztályok az objektumorientált programozás alapvető építőelemei. Egy osztály adattagokat (mezők) és metódusokat (függvények) tartalmazhat.

**Jellemzők**:
- **Encapsuláció**: Az adatokat és a viselkedést egyetlen egységbe foglalja össze.
- **Öröklődés**: Egy osztály örökölheti egy másik osztály tulajdonságait.
- **Polimorfizmus**: Azonos nevű metódusok különböző osztályokban eltérően működhetnek.

**Példa (C++)**:
```cpp
class Person {
public:
    string name;
    int age;

    void display() {
        cout << "Name: " << name << ", Age: " << age << endl;
    }
};
```

**Struct (struktúra)**

**Definíció**: A struktúrák olyan adatstruktúrák, amelyek különböző típusú elemeket tartalmazhatnak, hasonlóan az osztályokhoz, de általában kevesebb funkcionalitással rendelkeznek.

**Példa (C++)**:
```cpp
struct Person {
    string name;
    int age;
};
```

### Felsorolásos típusok

**Definíció**: A felsorolásos típusok (enumeration) olyan adatstruktúrák, amelyek egy azonosítóval ellátott állandó értékek halmazát definiálják.

**Példa (C++)**:
```cpp
enum Color { RED, GREEN, BLUE };
```

**Példa (C#)**:
```csharp
enum Color { Red, Green, Blue }
```

### Metódusok

**Definíció**: A metódusok olyan függvények, amelyek egy osztály vagy struktúra részét képezik, és amelyek az adott objektum állapotát kezelik vagy módosítják.

**Példa (C++)**:
```cpp
class MyClass {
public:
    void myMethod() {
        // Metódus törzse
    }
};
```

**Példa (Python)**:
```python
class MyClass:
    def my_method(self):
        # Metódus törzse
```

### Paraméterátadás módjai, változó paraméterszám

**Paraméterátadás módjai**

1. **Érték szerinti átadás (Pass by Value)**: Az argumentum másolatát adja át a függvénynek.
2. **Referencia szerinti átadás (Pass by Reference)**: Az argumentum memóriacímét adja át a függvénynek, így a változás a hívó fél számára is látható.
3. **Cím szerinti átadás (Pass by Address)**: Az argumentum mutatóját adja át a függvénynek.

**Példa (C++)**:
```cpp
void byValue(int a) { a = 10; }
void byReference(int &a) { a = 10; }
void byAddress(int *a) { *a = 10; }
```

**Változó paraméterszám**

Néhány programozási nyelv támogatja a változó számú paraméterek átadását.

**Példa (C variadic functions)**:
```c
#include <stdarg.h>
void printNumbers(int num, ...) {
    va_list arguments;
    va_start(arguments, num);
    for (int i = 0; i < num; i++) {
        printf("%d ", va_arg(arguments, int));
    }
    va_end(arguments);
}
```

**Példa (Python)**:
```python
def print_numbers(*args):
    for arg in args:
        print(arg)
```

### Programozási nyelvek fordítási és futtatási megoldásai

**Fordítási módok**:
1. **Fordított nyelvek (Compiled Languages)**: A forráskódot gépi kódra fordítják egy fordítóprogrammal (pl. C, C++).
2. **Értelmezett nyelvek (Interpreted Languages)**: A forráskódot egy értelmező futtatja soronként (pl. Python, JavaScript).
3. **Félig fordított nyelvek (Hybrid Languages)**: A forráskódot egy köztes bájtkódra fordítják, amit egy virtuális gép futtat (pl. Java, C#).

**Példa (C)**:
```bash
gcc program.c -o program
./program
```

**Példa (Python)**:
```bash
python program.py
```

### .NET keretrendszer felépítése

**Definíció**: A .NET keretrendszer egy platformfüggetlen környezet, amely támogatja a különböző programozási nyelvek alkalmazásainak fejlesztését és futtatását.

**Főbb komponensek**:
- **Common Language Runtime (CLR)**: A .NET futtatókörnyezete, amely kezeli a memóriát, a biztonságot, a kivételkezelést stb.
- **.NET osztálykönyvtárak (Framework Class Library, FCL)**: A különböző osztályok és függvények gyűjteménye, amelyek segítik a fejlesztést.
- **ASP.NET**: Webalkalmazások és webszolgáltatások fejlesztésére szolgáló keretrendszer.
- **ADO.NET**: Adatbázisokhoz való hozzáférést biztosít.

**Példa (C#)**:
```csharp
using System;

class Program {
    static void Main() {
        Console.WriteLine("Hello, World!");
    }
}
```

### Más programozási nyelvek és keretrendszerek

1. **Java és JDK (Java Development Kit)**: A Java platform része, amely a fejlesztéshez szükséges eszközöket tartalmazza, mint például a javac fordító.
2. **Python és Django**: A Python egy magas szintű, dinamikus programozási nyelv. A Django egy webalkalmazás-fejlesztő keretrendszer Pythonhoz.
3. **JavaScript és Node.js**: A JavaScript egy szkriptnyelv, amelyet főként webfejlesztéshez használnak. A Node.js lehetővé teszi a JavaScript futtatását a szerveroldalon.
4. **Ruby és Ruby on Rails**: A Ruby egy dinamikus, objektumorientált programozási nyelv. A Ruby on

 Rails egy webalkalmazás-fejlesztő keretrendszer Rubyhoz.

Mindezek a nyelvek és keretrendszerek különböző célokra használhatók, és a választás a konkrét fejlesztési igényektől függ.