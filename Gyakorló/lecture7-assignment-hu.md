# 7. Gyakorló Feladatsor: Gyűjtemények

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni a Gyűjtemény Keretrendszer fogalmakat, amelyeket a 7. előadásban tanultál. Dolgozol ArrayList, HashMap, HashSet típusokkal és implementálsz fejlett adatkezelést gyűjteményekkel.

## 🎯 Tanulási Célok
- Gyűjtemény Keretrendszer használat gyakorlása
- Megtanulni az ArrayList, HashMap, HashSet hatékony használatát
- Gyűjtemény műveletek és algoritmusok gyakorlása
- Generikus típusok és típusbiztonság megértése
- Fejlett adatkezelés implementálása
- Megfelelő gyűjtemény típusok kiválasztása

## 📝 Feladat Feladatok

### Feladat 1: Diák Menedzser Gyűjteményekkel (30 pont)
Hozz létre egy DiákMenedzser osztályt a Gyűjtemény Keretrendszer használatával:

**Követelmények:**
- **Használandó gyűjtemények**:
  - ArrayList<Student> diákok tárolásához
  - HashMap<String, Student> gyors kereséshez azonosító szerint
  - HashSet<String> egyedi diákazonosítókhoz
  - HashMap<String, List<Student>> diákok osztály szerint
- **Implementálandó metódusok**:
  - addStudent(Student student)
  - removeStudent(String studentId)
  - findStudentById(String studentId)
  - findStudentsByName(String name)
  - findStudentsByGrade(String grade)
  - findHighAchievers(double minGpa)
  - getStudentsSortedByGpa()
  - getStudentsSortedByName()
  - displayAllStudents()
  - displayStatistics()

**Várható kimenet:**
```
=== Diák Menedzser Gyűjteményekkel ===
Diák hozzáadva: Kovács Anna
Diák hozzáadva: Nagy Péter
Összes diák: 2

=== Összes Diák ===
1. Kovács Anna (STU001) - 10. osztály - Átlag: 3.5 - Jó
2. Nagy Péter (STU002) - 9. osztály - Átlag: 3.8 - Jó
```

### Feladat 2: Átlag Statisztikák Gyűjteményekkel (25 pont)
Implementálj átlag statisztikákat gyűjtemények használatával:

**Követelmények:**
- **Statisztikai metódusok**:
  - getAverageGpa()
  - getHighestGpa()
  - getLowestGpa()
  - getGpaStatistics()
  - getGradeDistribution()
  - getAgeDistribution()
- **Gyűjtemény műveletek**:
  - Használd a stream-eket a számításokhoz
  - Implementálj rendezési algoritmusokat
  - Csoportosítsd a diákokat kritériumok szerint
  - Számítsd ki a statisztikákat hatékonyan

**Várható kimenet:**
```
=== Átlag Statisztikák ===
Összes diák: 5
Átlagos átlag: 3.4
Legmagasabb átlag: 3.9
Legalacsonyabb átlag: 2.8

Osztály eloszlás:
  9. osztály: 2 diák
  10. osztály: 2 diák
  11. osztály: 1 diák

Életkor eloszlás:
  Életkor 15: 1 diák
  Életkor 16: 2 diák
  Életkor 17: 2 diák
```

### Feladat 3: Gyűjtemény Műveletek (20 pont)
Gyakorold a különböző gyűjtemény műveleteket:

**Követelmények:**
- **Rendezési műveletek**:
  - Rendezd a diákokat név szerint (növekvő)
  - Rendezd a diákokat átlag szerint (csökkenő)
  - Rendezd a diákokat életkor szerint (növekvő)
- **Keresési műveletek**:
  - Találj diákokat átlag küszöb felett
  - Találj diákokat életkor tartományban
  - Találj diákokat osztály szint szerint
- **Halmaz műveletek**:
  - Szerezd meg az egyedi osztályokat
  - Szerezd meg az egyedi életkorokat
  - Találj közös elemeket

**Várható kimenet:**
```
=== Gyűjtemény Műveletek ===
Diákok név szerint rendezve:
1. Kovács Anna (STU001) - Átlag: 3.5
2. Nagy Péter (STU002) - Átlag: 3.8
3. Szabó Mária (STU003) - Átlag: 3.2

Diákok átlag szerint rendezve (csökkenő):
1. Nagy Péter (STU002) - Átlag: 3.8
2. Kovács Anna (STU001) - Átlag: 3.5
3. Szabó Mária (STU003) - Átlag: 3.2

Egyedi osztályok: [9. osztály, 10. osztály, 11. osztály]
```

### Feladat 4: Fejlett Adatkezelés (25 pont)
Implementálj fejlett adatkezelést gyűjteményekkel:

**Követelmények:**
- **Adat csoportosítás**:
  - Csoportosítsd a diákokat osztály szint szerint
  - Csoportosítsd a diákokat életkor tartomány szerint
  - Csoportosítsd a diákokat átlag tartomány szerint
- **Adat elemzés**:
  - Találj top teljesítőket
  - Találj támogatásra szoruló diákokat
  - Számítsd ki az osztály statisztikákat
  - Generálj jelentéseket
- **Gyűjtemény segédeszközök**:
  - Implementálj adat validációt
  - Kezeld a duplikált adatokat
  - Biztosítsd az adat export funkcionalitást

**Várható kimenet:**
```
=== Fejlett Adatkezelés ===
Diákok osztály szint szerint:
Alapfokú (9-10. osztály): 4 diák
Középfokú (11-12. osztály): 1 diák

Diákok átlag tartomány szerint:
Kiváló (3.7+): 2 diák
Jó (3.0-3.6): 2 diák
Átlagos (2.0-2.9): 1 diák

Top teljesítők:
1. Nagy Péter (STU002) - Átlag: 3.8
2. Kovács Anna (STU001) - Átlag: 3.5

Támogatásra szoruló diákok:
1. Szabó Mária (STU003) - Átlag: 2.8
```

## 📁 Fájl Struktúra
Hozd létre a következő fájlokat a `lecture7` könyvtárban:
```
src/main/java/lecture7/
├── Student.java
├── StudentManager.java
├── GradeStatistics.java
├── CollectionOperations.java
└── AdvancedDataManagement.java
```


### Fájl elnevezési konvenció:
- Java fájlok: `Student.java`, `StudentManager.java`, stb.
- Képernyőképek: `Student-output.png`, `StudentManager-output.png`, stb.
- Dokumentáció: `gyujtemeny-magyarazatok.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj az ArrayList-tel**: A legkönnyebb gyűjtemény megérteni
2. **Használj generikusokat**: Mindig használj generikus típusokat a típusbiztonságért
3. **Gyakorold az iterációt**: Tanulj meg különböző módokon iterálni
4. **Értsd meg a teljesítményt**: Tudd, mikor melyik gyűjteményt használni
5. **Teszteld a műveleteket**: Ellenőrizd, hogy a gyűjtemény műveletek működnek

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Generikusok nem használata**: Nyers típusok használata generikus típusok helyett
2. **Gyűjtemény típusok összekeverése**: Hibás gyűjtemény használata a feladathoz
3. **Módosítás iteráció közben**: Gyűjtemény módosítása iteráció közben
4. **Null kezelés**: Null értékek ellenőrzésének elmulasztása
5. **Teljesítmény problémák**: Hibás gyűjtemény használata teljesítmény követelményekhez

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett Gyűjtemények
- Implementálj egyedi gyűjteményeket
- Használj fejlett gyűjtemény algoritmusokat
- Implementálj gyűjtemény komparátorokat
- Hozz létre gyűjtemény segédeszközöket

### Bónusz 2: Teljesítmény Optimalizálás
- Optimalizáld a gyűjtemény műveleteket
- Implementálj hatékony keresést
- Használj megfelelő gyűjtemény típusokat
- Mérj teljesítmény különbségeket

### Bónusz 3: Gyűjtemény Tervezési Minták
- Implementálj gyűjtemény gyárakat
- Hozz létre gyűjtemény építőket
- Implementálj gyűjtemény dekorátorokat
- Használj gyűjtemény adaptereket

---

**Sok sikert a gyűjtemények feladatához! Ne feledd, a gyűjtemények hatékony adatkezeléshez nélkülözhetetlen eszközök! 🚀**
