# 2. Gyakorló Feladat: Java Alapok

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni a Java programozás alapjait, amelyeket a 2. előadásban tanultál. Létrehozol osztályokat, objektumokat és megismerkedel az objektum-orientált programozás alapjaival.

## 🎯 Tanulási Célok
- Osztályok és objektumok megértése
- Konstruktorok és metódusok használata
- Adattípusok és változók kezelése
- Alapvető programozási struktúrák
- Objektum-orientált gondolkodás

## 📝 Feladat Feladatok

### Feladat 1: Diák Osztály (30 pont)
Hozz létre egy egyszerű Diák osztályt:

**Követelmények:**
- **Fájl neve**: `Student.java`
- **Mezők**: név, életkor, email, telefonszám, diákazonosító, osztály
- **Konstruktorok**: alapértelmezett, paraméterezett
- **Metódusok**: getterek, setterek, `displayInfo()`
- **Adatvalidáció**: érvényes adatok ellenőrzése

**Várható kimenet:**
```
=== Diák Információ ===
Név: Kovács Anna
Életkor: 16
Email: anna.kovacs@email.com
Telefon: +36-30-123-4567
Diákazonosító: STU001
Osztály: 10.A
========================
```

### Feladat 2: Diák Menedzser (25 pont)
Hozz létre egy DiákMenedzser osztályt:

**Követelmények:**
- **Fájl neve**: `StudentManager.java`
- **Mezők**: diákok tömbje, diákok száma, maximális kapacitás
- **Metódusok**:
  - `addStudent(Student student)` - diák hozzáadása
  - `removeStudent(int index)` - diák eltávolítása
  - `findStudentByName(String name)` - diák keresése név szerint
  - `displayAllStudents()` - összes diák megjelenítése
  - `getStudentCount()` - diákok száma
- **Tömbkezelés**: dinamikus tömbkezelés

**Várható kimenet:**
```
=== Diák Menedzser ===
Diák hozzáadva: Kovács Anna
Diák hozzáadva: Nagy Péter
Összes diák: 2

=== Összes Diák ===
1. Kovács Anna (STU001) - 10.A
2. Nagy Péter (STU002) - 9.B
```

### Feladat 3: Főprogram (20 pont)
Hozz létre egy főprogramot a rendszer teszteléséhez:

**Követelmények:**
- **Fájl neve**: `Main.java`
- **Funkciók**:
  - DiákMenedzser létrehozása
  - Diákok hozzáadása
  - Diákok megjelenítése
  - Keresési funkciók tesztelése
  - Statisztikák megjelenítése
- **Interakció**: felhasználói bemenet kezelése

**Várható kimenet:**
```
=== Iskolai Rendszer ===
DiákMenedzser inicializálva: 5 diák kapacitással

Diák hozzáadva: Kovács Anna
Diák hozzáadva: Nagy Péter
Diák hozzáadva: Szabó Mária

Keresés: Kovács Anna
Találat: Kovács Anna (STU001) - 10.A

Statisztikák:
Összes diák: 3
Kapacitás: 5
Szabad hely: 2
```

### Feladat 4: Adatvalidáció és Hibakezelés (25 pont)
Implementálj adatvalidációt és hibakezelést:

**Követelmények:**
- **Adatvalidáció**:
  - Név nem lehet üres
  - Életkor 5-25 év között
  - Email tartalmazza a @ jelet
  - Telefonszám nem lehet üres
- **Hibakezelés**:
  - Érvénytelen adatok kezelése
  - Felhasználóbarát hibaüzenetek
  - Adatok javítása
- **Tesztelés**: különböző hibás adatokkal

**Várható kimenet:**
```
=== Adatvalidáció Tesztelés ===
Név: "" (üres)
Hiba: A név nem lehet üres!

Életkor: 30
Hiba: Az életkor 5-25 év között kell legyen!

Email: "rossz-email"
Hiba: Az email tartalmaznia kell a @ jelet!

Telefon: "" (üres)
Hiba: A telefonszám nem lehet üres!

Minden adat érvényesítve!
```

## 📁 Fájl Struktúra
Hozd létre a következő fájlokat a `lecture2` könyvtárban:
```
src/main/java/lecture2/
├── Student.java
├── StudentManager.java
└── Main.java
```

## 💡 Sikerhez vezető tippek

1. **Kezdj az osztályokkal**: Definiáld az osztályokat először
2. **Használj konstruktorokat**: Inicializáld az objektumokat
3. **Implementálj metódusokat**: Adj funkcionalitást az osztályoknak
4. **Validáld az adatokat**: Ellenőrizd a bemeneti adatokat
5. **Teszteld a kódot**: Futtasd és teszteld a programokat

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Hiányzó konstruktorok**: Minden osztálynak kell konstruktor
2. **Hibás metódus szignatúrák**: Figyelj a paraméterekre
3. **Nem validált adatok**: Mindig validáld a bemeneti adatokat
4. **Rossz elnevezés**: Használj beszédes változó- és metódusneveket
5. **Nem tesztelt kód**: Mindig teszteld a programokat

## 📚 További források

- Tekintsd át az előadás jegyzeteket és kód példákat
- Gyakorolj a megadott mintaprogramokkal
- Használj online Java dokumentációt referenciaként
- Kérdezz órák alatt

### Bónusz 1: Fejlett Diák Osztály
- Adj hozzá további mezőket (születési dátum, cím, stb.)
- Implementálj összehasonlító metódusokat
- Adj hozzá statisztikai metódusokat
- Készíts diák jelentéseket

### Bónusz 2: Keresési Funkciók
- Implementálj különböző keresési módszereket
- Adj hozzá szűrési lehetőségeket
- Implementálj rendezési funkciókat
- Készíts keresési statisztikákat

### Bónusz 3: Adat Export/Import
- Implementálj adat mentést fájlba
- Adj hozzá adat betöltést fájlból
- Implementálj CSV formátum támogatást
- Készíts adat biztonsági mentést

---

**Sok sikert a Java alapok feladatához! Ne feledd, a jó objektum-orientált programozás az alapokkal kezdődik! 🚀**
