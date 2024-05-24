# Magasszintű programozási nyelvek II

## Az OOP alapelvei, alapfogalmai

Az objektumorientált programozás (OOP) egy programozási paradigma, amely az objektumok fogalmán alapul. Az OOP alapelvei közé tartozik az öröklés, az enkapszuláció, a polimorfizmus és az absztrakció.

### Alapelvek

1. **Öröklés (Inheritance)**: Lehetővé teszi, hogy egy új osztály (leszármazott) egy már létező osztály (szülő) tulajdonságait és metódusait örökölje.

2. **Enkapszuláció (Encapsulation)**: Az adatok és a metódusok elrejtése és védelme, hogy a belső állapotot közvetlenül ne lehessen módosítani kívülről.

3. **Polimorfizmus (Polymorphism)**: Lehetővé teszi, hogy különböző osztályok objektumai ugyanazokat a metódusokat hívják meg, de az adott osztály specifikus implementációját használják.

4. **Absztrakció (Abstraction)**: Az adatok és az operációk elrejtése, amely csak a lényeges tulajdonságokat és viselkedéseket emeli ki.

## Alapfogalmak

### Mezők (Fields)

A mezők az osztály adattagjai, amelyek tárolják az objektum állapotát.

```csharp
class Person {
    private string name;
    public int age;
}
```

### Metódusok (Methods)

A metódusok az osztály viselkedését határozzák meg, és műveleteket végeznek az adatokon.

```csharp
class Person {
    public void Greet() {
        Console.WriteLine("Hello!");
    }
}
```

### Property-k (Properties)

A property-k olyan speciális mezők, amelyek getter és setter metódusokkal rendelkeznek, így szabályozva az adatok hozzáférését és módosítását.

```csharp
class Person {
    private string name;
    public string Name {
        get { return name; }
        set { name = value; }
    }
}
```

### Adatrejtés (Encapsulation)

Az adatrejtés az osztály belső állapotának védelmét jelenti. Az adatokhoz való hozzáférést kontrollálják a getter és setter metódusok.

```csharp
class Person {
    private string name;
    public string Name {
        get { return name; }
        set { name = value; }
    }
}
```

## Konténerosztályok használata és indexelők

### Konténerosztályok

A konténerosztályok olyan osztályok, amelyek más objektumok gyűjteményét kezelik. Példák: `List<T>`, `Dictionary<TKey, TValue>`.

```csharp
List<int> numbers = new List<int> {1, 2, 3};
Dictionary<string, int> ages = new Dictionary<string, int> {
    {"Alice", 30},
    {"Bob", 25}
};
```

### Indexelők

Az indexelők lehetővé teszik az osztályok objektumainak úgynevezett "tömbszerű" elérését.

```csharp
class SampleCollection<T> {
    private T[] arr = new T[100];
    public T this[int i] {
        get { return arr[i]; }
        set { arr[i] = value; }
    }
}
```

## Osztályszint és példányszint

### Osztályszintű tagok (Class-level members)

Az osztályszintű tagok statikusak, és az osztályhoz tartoznak, nem pedig egy konkrét példányhoz.

```csharp
class MyClass {
    public static int counter = 0;
}
```

### Példányszintű tagok (Instance-level members)

A példányszintű tagok az osztály konkrét példányaihoz tartoznak, és minden példánynak saját példányszintű tagjai vannak.

```csharp
class MyClass {
    public int instanceCounter = 0;
}
```

## Névterek (Namespaces)

A névterek logikai csoportosításokat biztosítanak az osztályok, interfészek, enumerációk és egyéb típusok számára, ezzel elkerülve a névütközéseket.

```csharp
namespace MyApplication {
    class MyClass {
        // Osztály tartalma
    }
}
```

## Bővítő metódusok (Extension methods)

A bővítő metódusok lehetővé teszik meglévő osztályok funkcionalitásának kiterjesztését anélkül, hogy módosítanánk azokat.

```csharp
public static class StringExtensions {
    public static bool IsPalindrome(this string str) {
        // Metódus implementációja
    }
}
```

## Operátor overloading (Operátor túlterhelés)

Az operátor túlterhelés lehetővé teszi, hogy meghatározzuk, hogyan viselkedjenek az operátorok az általunk definiált osztályok példányain.

```csharp
class Complex {
    public int Real { get; set; }
    public int Imaginary { get; set; }

    public static Complex operator +(Complex c1, Complex c2) {
        return new Complex {
            Real = c1.Real + c2.Real,
            Imaginary = c1.Imaginary + c2.Imaginary
        };
    }
}
```

Ezek az alapelvek és fogalmak segítenek az OOP megértésében és alkalmazásában különböző magasszintű programozási nyelvekben, mint például C#, Java és C++.