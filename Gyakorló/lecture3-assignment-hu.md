# 3. Gyakorló Feladat: OOP Alapok

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni az Objektum-Orientált Programozás alapjait, amelyeket a 3. előadásban tanultál. Létrehozol fejlett osztályokat megfelelő kapszulázással, konstruktorokkal és metódusokkal.

## 🎯 Tanulási Célok
- Encapsulation gyakorlása
- Konstruktorok és konstruktor túlterhelés megértése
- Getter és setter metódusok implementálása
- Metódus túlterhelés (method overloading) gyakorlása
- Adatvalidáció implementálása
- Jól strukturált osztályok tervezése

## 📝 Feladat Feladatok

### Feladat 1: Fejlett Diák Osztály (30 pont)
Hozz létre egy fejlett Diák osztályt megfelelő kapszulázással:

**Követelmények:**
- **Fájl neve**: `EnhancedStudent.java`
- **Privát mezők**: név, életkor, diákazonosító, osztály, átlag, email, telefonszám, szülő neve, vészhelyzeti kapcsolat
- **Konstruktorok**:
  - Alapértelmezett konstruktor
  - Alapvető információk konstruktora (név, életkor, diákazonosító, osztály)
  - Teljes konstruktor minden mezővel
- **Getter metódusok**: minden mezőhöz
- **Setter metódusok**: validációval minden mezőhöz
- **Metódus túlterhelés**:
  - `updateGpa(double gpa)` és `updateGpa(String gpaString)`
  - `setContactInfo(String email, String phone)` és `setContactInfo(String email, String phone, String emergency)`
- **Validációs szabályok**:
  - Név: nem lehet üres, trimelt
  - Életkor: 5-25 év között
  - Diákazonosító: nem lehet üres, nagybetűs
  - Osztály: nem lehet üres
  - Átlag: 0.0 és 4.0 között
  - Email: tartalmazza a @ jelet
  - Telefon: nem lehet üres
  - Szülő neve: nem lehet üres
  - Vészhelyzeti kapcsolat: nem lehet üres

**Várható kimenet:**
```
Diák: Kovács Anna (STU001) - 10. osztály - Átlag: 3.5
Kapcsolat: anna@email.com, +36-30-123-4567
Szülő: Kovács Péter, Vészhelyzeti: +36-30-987-6543
```

### Feladat 2: Iskola Osztály Menedzser Rendszer (25 pont)
Hozz létre egy IskolaOsztály osztályt megfelelő kapszulázással:

**Követelmények:**
- **Fájl neve**: `SchoolClass.java`
- **Privát mezők**: osztályNév, tantárgy, tanárNév, maxKapacitás, jelenlegiLétszám, teremSzám, órarend, aktív
- **Konstruktorok**:
  - Alapértelmezett konstruktor
  - Alapvető konstruktor (osztályNév, tantárgy, tanárNév)
  - Teljes konstruktor (minden mező)
- **Getter metódusok**: minden mezőhöz
- **Setter metódusok**: validációval
- **Metódus túlterhelés**:
  - `enrollStudent()` és `enrollStudent(int numberOfStudents)`
  - `updateClassInfo(String teacher, String room)` és `updateClassInfo(String teacher, String room, String schedule)`
- **Üzleti logikai metódusok**:
  - `getAvailableSpots()`
  - `getEnrollmentPercentage()`
  - `isFull()`
  - `isEmpty()`
  - `getClassStatus()`

**Validációs szabályok**:
- Osztály név: nem lehet üres
- Tantárgy: nem lehet üres
- Tanár név: nem lehet üres
- Max kapacitás: 1-50 között
- Terem szám: nem lehet üres
- Órarend: nem lehet üres

### Feladat 3: Adatvalidációs Segédeszköz (20 pont)
Hozz létre egy AdatValidátor osztályt statikus metódusokkal:

**Követelmények:**
- **Fájl neve**: `DataValidator.java`
- **Statikus metódusok**:
  - `validateName(String name)`
  - `validateAge(int age)`
  - `validateEmail(String email)`
  - `validatePhone(String phone)`
  - `validateGpa(double gpa)`
  - `validateStudentId(String studentId)`
- **Visszatérési típusok**: boolean (true ha érvényes, false ha érvénytelen)
- **Hibaüzenetek**: megfelelő hibaüzenetek kiírása érvénytelen adatokhoz
- **Segédmetódusok**:
  - `isValidString(String str)` - ellenőrzi, hogy a string nem null és nem üres
  - `containsOnlyLetters(String str)` - ellenőrzi, hogy a string csak betűket tartalmaz
  - `containsOnlyDigits(String str)` - ellenőrzi, hogy a string csak számokat tartalmaz

### Feladat 4: Diák Menedzser Validációval (25 pont)
Hozz létre egy DiákMenedzser osztályt, amely a fejlett osztályokat használja:

**Követelmények:**
- **Fájl neve**: `StudentManager.java`
- **Mezők**: EnhancedStudent objektumok tömbje, jelenlegi szám
- **Metódusok**:
  - `addStudent(EnhancedStudent student)` - validációval
  - `findStudentById(String studentId)` - kis- és nagybetű nem érzékeny keresés
  - `updateStudentGpa(String studentId, double newGpa)` - validációval
  - `displayAllStudents()`
  - `displayStudentsByGrade(String grade)`
  - `getStatistics()` - összes diák, átlagos átlag, osztály eloszlás
- **Validáció**: AdatValidátor osztály használata minden validációhoz
- **Hibakezelés**: érvénytelen adatok kezelése graciálisan

## 📁 Fájl Struktúra
Hozd létre a következő fájlokat a `lecture3` könyvtárban:
```
src/main/java/lecture3/
├── EnhancedStudent.java
├── SchoolClass.java
├── DataValidator.java
└── StudentManager.java
```

### Fájl elnevezési konvenció:
- Java fájlok: `EnhancedStudent.java`, `SchoolClass.java`, stb.
- Képernyőképek: `EnhancedStudent-output.png`, `SchoolClass-output.png`, stb.
- Dokumentáció: `validacios-logika.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj a mezőkkel**: Definiáld az összes privát mezőt először
2. **Készíts konstruktorokat**: Kezdj alapértelmezett, majd add hozzá a paraméterezetteket
3. **Adj hozzá gettereket**: Egyszerű metódusok a mező értékek visszaadásához
4. **Implementálj settereket**: Adj hozzá validációt minden setterhez
5. **Implementálj túlterhelést**: Adj hozzá túlterhelt metódusokat a rugalmassághoz

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Felejtett validáció**: Ne validáld az adatokat setterekben
2. **Nyilvános mezők**: Ne tedd a mezőket nyilvánossá getter/setter helyett
3. **Hiányzó konstruktorok**: Ne hozz létre túl sok konstruktort
4. **Hibás túlterhelés**: Metódusoknak különböző paraméterekkel kell rendelkezniük
5. **Nincs hibaüzenet**: Ne adj hozzá egyértelmű hibaüzeneteket érvénytelen adatokhoz

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett Validáció
- Adj hozzá regex validációt email formátumhoz
- Implementálj telefonszám formátum validációt
- Adj hozzá diákazonosító formátum validációt (pl. STU után 3 számjegy)

### Bónusz 2: Fejlett Hibakezelés
- Hozz létre egyedi kivétel osztályokat validációs hibákhoz
- Implementálj try-catch blokkokat hibakezeléshez
- Adj hozzá naplózást validációs hibákhoz
- Készíts hibakezelési jelentéseket

### Bónusz 3: Adat Megőrzés
- Adj hozzá metódusokat diák adatok mentéséhez fájlba
- Implementálj adat betöltési funkcionalitást
- Adj hozzá adat biztonsági mentési funkcionalitást
- Készíts adat export CSV formátumba

---

**Sok sikert az OOP alapok feladatához! Ne feledd, a jó objektum-orientált tervezés a megfelelő kapszulázással kezdődik! 🚀**
