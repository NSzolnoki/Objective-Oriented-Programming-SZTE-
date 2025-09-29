# 6. Gyakorló Feladat: Absztrakt Osztályok és Interfészek

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni az absztrakt osztályok és interfészek fogalmakat, amelyeket a 6. előadásban tanultál. Létrehozol absztrakt osztályokat, implementálsz interfészeket és gyakorlod a szerződés-alapú programozást.

## 🎯 Tanulási Célok
- Absztrakt osztály létrehozás gyakorlása
- Interfész implementáció megértése
- Szerződés-alapú programozás gyakorlása
- Metódus felülírás gyakorlása absztrakt osztályokban
- Több interfész implementálása
- Interfészek alapértelmezett metódusainak használata

## 📝 Feladat Feladatok

### Feladat 1: Absztrakt Személy Osztály (30 pont)
Hozz létre egy absztrakt Személy osztályt konkrét és absztrakt metódusokkal:

**Követelmények:**
- **Absztrakt Személy Osztály**:
  - Mezők: név, életkor, email, telefonszám, cím
  - Konstruktorok: alapértelmezett, paraméterezett, teljes
  - Konkrét metódusok: getterek, setterek, getAgeCategory(), isMinor()
  - Absztrakt metódusok: getRole(), getStatus(), displayInfo()
  - Sablon metódus: displayPersonTemplate()
- **Konkrét Leszármazottak**:
  - Diák extends Személy
  - Tanár extends Személy
  - Adminisztrátor extends Személy
- **Metódus Implementáció**:
  - Minden leszármazottnak implementálnia kell az absztrakt metódusokat
  - Használd a @Override annotációt
  - Adj meg specifikus implementációkat

**Várható kimenet:**
```
=== Diák Információ ===
Név: Kovács Anna
Életkor: 20
Email: anna@email.com
Szerep: Diák
Státusz: Aktív Diák
Diákazonosító: STU001
Átlag: 3.5
========================
```

### Feladat 2: Interfész Implementáció (25 pont)
Hozz létre és implementálj interfészeket a gyakori viselkedésekhez:

**Követelmények:**
- **Értékelhető Interfész**:
  - Metódusok: getGrade(), setGrade(), getGradeStatus(), isPassing()
  - Konstansok: MIN_GRADE, MAX_GRADE, PASSING_GRADE
  - Alapértelmezett metódusok: isExcellent(), isGood(), getGradeDescription()
  - Statikus metódusok: gpaToPercentage(), getGradeLetter()
- **Részvételi Interfész**:
  - Metódusok: getAttendancePercentage(), setAttendance(), getAttendanceStatus()
  - Konstansok: MIN_ATTENDANCE, MAX_ATTENDANCE, PASSING_ATTENDANCE
  - Alapértelmezett metódusok: isGoodAttendance(), getAttendanceDescription()
- **Jelentéskészítő Interfész**:
  - Metódusok: generateReport(), getReportTitle(), getReportSummary()
  - Alapértelmezett metódusok: generateSummaryReport(), generateHtmlReport()

**Várható kimenet:**
```
Diák: Kovács Anna
Átlag: 3.5 (Jó)
Részvétel: 95.0% (Kiváló)
Jelentés: Diák Akadémiai Jelentés
```

### Feladat 3: Több Interfész Implementáció (20 pont)
Implementálj több interfészt egyetlen osztályban:

**Követelmények:**
- **Fejlett Diák Osztály**:
  - Extends absztrakt Személy
  - Implements Értékelhető, Részvételi, Jelentéskészítő
  - Adj meg implementációkat minden interfész metódushoz
  - Használd az interfészek alapértelmezett metódusait
- **Fejlett Tanár Osztály**:
  - Extends absztrakt Személy
  - Implements Értékelhető, Jelentéskészítő
  - Adj meg implementációkat az interfész metódusokhoz
- **Interfész Demonstráció**:
  - Mutasd meg, hogyan implementálhatnak osztályok több interfészt
  - Demonstrálj interfész polimorfizmust
  - Használd az interfész metódusokat polimorf módon

**Várható kimenet:**
```
=== Több Interfész Implementáció ===
Diák implementálja: Értékelhető, Részvételi, Jelentéskészítő
Tanár implementálja: Értékelhető, Jelentéskészítő

Diák jelentés:
Átlag: 3.5 (Jó)
Részvétel: 95.0% (Kiváló)
Státusz: Aktív Diák

Tanár jelentés:
Átlag: 4.0 (Kiváló)
Státusz: Aktív Tanár
```

### Feladat 4: Megkötés-alapú Programozás (25 pont)
Demonstrálj Megkötés-alapú programozást interfészekkel:

**Követelmények:**
- **Interfész Megtkötések**:
  - Definiálj egyértelmű megkötéseket minden interfészhez
  - Biztosítsd, hogy minden implementáló osztály követi a megkötéseket
  - Validáld a megkötés betartását
- **Polimorf Viselkedés**:
  - Használd az interfészeket polimorf metódus hívásokhoz
  - Demonstrálj interfész-alapú programozást
  - Mutasd meg az interfész implementáció rugalmasságát
- **Megkötés Validáció**:
  - Validáld, hogy az osztályok implementálják az összes szükséges metódust
  - Ellenőrizd a megkötés betartását
  - Adj meg megkötés dokumentációt

**Várható kimenet:**
```
=== Megkötés-alapú Programozás ===
Értékelhető megkötés:
- getGrade(): double
- setGrade(double): boolean
- getGradeStatus(): String
- isPassing(): boolean

Részvételi Megkötés:
- getAttendancePercentage(): double
- setAttendance(double): boolean
- getAttendanceStatus(): String

Jelentéskészítő Megkötés:
- generateReport(): String
- getReportTitle(): String
- getReportSummary(): String

Minden megkötés sikeresen implementálva!
```

## 📁 Fájl Struktúra
Hozd létre a következő fájlokat a `lecture6` könyvtárban:
```
src/main/java/lecture6/
├── Person.java (absztrakt)
├── Student.java
├── Teacher.java
├── Administrator.java
├── Gradeable.java
├── Attendable.java
├── Reportable.java
└── InterfaceDemo.java
```

### Fájl elnevezési konvenció:
- Java fájlok: `Person.java`, `Gradeable.java`, stb.
- Képernyőképek: `Person-output.png`, `Gradeable-output.png`, stb.
- Dokumentáció: `abstrakcio-magyarazatok.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj az absztrakt osztállyal**: Hozd létre az absztrakt Személy osztályt először
2. **Definiálj egyértelmű szerződéseket**: Győződj meg róla, hogy az interfészeknek egyértelmű szerződéseik vannak
3. **Implementálj minden metódust**: Győződj meg róla, hogy minden absztrakt metódus implementálva van
4. **Használd az alapértelmezett metódusokat**: Vegyél igénybe az interfészek alapértelmezett metódusait
5. **Teszteld a szerződéseket**: Ellenőrizd, hogy a szerződések megfelelően implementálva vannak

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Absztrakt osztályok példányosítása**: Nem hozhatsz létre objektumokat absztrakt osztályokból
2. **Absztrakt metódusok implementálásának elfelejtése**: Implementálnod kell minden absztrakt metódust
3. **Hibás hozzáférés módosítók**: Az interfész metódusok alapértelmezetten nyilvánosak
4. **Körkörös függőségek**: Körkörös interfész függőségek létrehozása
5. **Hiányzó @Override**: Nem használod a @Override annotációt

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett Interfészek
- Hozz létre összetettebb interfészeket
- Implementálj interfész öröklést
- Adj hozzá statikus metódusokat az interfészekhez
- Hozz létre interfész hierarchiákat

### Bónusz 2: Alapértelmezett Metódusok
- Implementálj összetett alapértelmezett metódusokat
- Használd az alapértelmezett metódusokat a közös funkcionalitáshoz
- Írd felül az alapértelmezett metódusokat az implementáló osztályokban
- Hozz létre alapértelmezett metódus láncokat

### Bónusz 3: Interfész Polimorfizmus
- Implementálj interfész-alapú polimorfizmust
- Hozz létre polimorf gyűjteményeket interfészekkel
- Implementálj interfész gyárakat
- Hozz létre interfész-alapú tervezési mintákat

---

**Sok sikert az absztrakt osztályok és interfészek feladatához! Ne feledd, az absztrakt osztályok és interfészek biztosítják a rugalmas, bővíthető tervezés alapját! 🚀**
