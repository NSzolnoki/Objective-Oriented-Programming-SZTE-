# 4. Gyakorló Feladat: OOP Kapcsolatok

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni az Objektum-Orientált Programozás kapcsolatait, amelyeket a 4. előadásban tanultál. Létrehozol osztályokat különböző típusú kapcsolatokkal és megtanulod az objektum kapcsolatok kezelését.

## 🎯 Tanulási Célok
- Osztály kapcsolatok és kapcsolatok gyakorlása
- Megtanulni az aggregáció és kompozíció implementálását
- Objektum életciklus kezelésének megértése
- Valós kapcsolatok modellezése kódban
- Kapcsolatok tervezése osztályok között
- Objektum függőségek kezelése

## 📝 Feladat Feladatok

### Feladat 1: Tantárgy-Osztály Kapcsolat (25 pont)
Hozz létre egy Tantárgy osztályt és hozz létre kapcsolatot az IskolaOsztály osztállyal:

**Követelmények:**
- **Tantárgy Osztály**:
  - Mezők: tantárgyKód, tantárgyNév, leírás, kreditÓrák, tanszék
  - Konstruktorok: alapértelmezett, paraméterezett, teljes
  - Metódusok: getterek, setterek, validáció, displayInfo()
- **IskolaOsztály Osztály**:
  - Mezők: osztályNév, tantárgy (kapcsolat), tanárNév, maxKapacitás, jelenlegiLétszám
  - Metódusok: assignSubject(), getSubjectInfo(), displayClassWithSubject()
- **Kapcsolat Kapcsolat**:
  - IskolaOsztály rendelkezik Tantárgy-val
  - Tantárgy hozzárendelhető több osztályhoz
  - Implementálj metódusokat a kapcsolat kezeléséhez

**Várható kimenet:**
```
Osztály: Matematika 101
Tantárgy: Algebra (MATH101) - 3 kredit - Matematika Tanszék
Tanár: Dr. Kovács
Kapacitás: 25 diák
```

### Feladat 2: Diák-Osztály Aggregáció (30 pont)
Implementálj az aggregáció kapcsolatot a Diák és IskolaOsztály között:

**Követelmények:**
- **Fejlett Diák Osztály**:
  - Adj hozzá mezőket: felvettOsztályok (tömb), osztálySzámláló
  - Metódusok: enrollInClass(), unenrollFromClass(), getEnrolledClasses()
- **Fejlett IskolaOsztály Osztály**:
  - Adj hozzá mezőket: felvettDiákok (tömb), diákSzámláló
  - Metódusok: addStudent(), removeStudent(), getEnrolledStudents()
- **Aggregáció Kapcsolat**:
  - Diákok feliratkozhatnak több osztályba
  - Osztályoknak lehet több diákja
  - Diákok és osztályok függetlenül létezhetnek

**Várható kimenet:**
```
Diák: Kovács Anna (STU001)
Felvett osztályok: Matematika 101, Angol 201, Természettudomány 301

Osztály: Matematika 101
Felvett diákok: Kovács Anna, Nagy Péter, Szabó Mária
```

### Feladat 3: Kapcsolat Menedzser (25 pont)
Hozz létre egy KapcsolatMenedzser osztályt az összes kapcsolat kezeléséhez:

**Követelmények:**
- **Mezők**: tantárgyak (tömb), osztályok (tömb), diákok (tömb)
- **Metódusok**:
  - addSubject(), addClass(), addStudent()
  - findSubjectByCode(), findClassByName(), findStudentById()
  - assignSubjectToClass(), enrollStudentInClass()
  - displayAllRelationships(), getRelationshipStatistics()
- **Kapcsolat Kezelés**:
  - Tantárgy-osztály kapcsolatok nyomon követése
  - Diák-osztály feliratkozások nyomon követése
  - Kapcsolat elemzés biztosítása

**Várható kimenet:**
```
=== Kapcsolat Elemzés ===
Összes tantárgy: 5
Összes osztály: 8
Összes diák: 25
Tantárgyak osztályok nélkül: 1
Osztályok tantárgyak nélkül: 0
Diákok osztályok nélkül: 3
```

### Feladat 4: Kompozíció Példa (20 pont)
Hozz létre egy kompozíció kapcsolat példát:

**Követelmények:**
- **Cím Osztály**:
  - Mezők: utca, város, állam, irányítószám
  - Metódusok: getFullAddress(), validateAddress()
- **Fejlett Diák Osztály**:
  - Adj hozzá mezőt: cím (kompozíció)
  - Metódusok: setAddress(), getAddress(), updateAddress()
- **Kompozíció Kapcsolat**:
  - Diák birtokolja a Címet
  - Cím nem létezhet Diák nélkül
  - Implementálj megfelelő életciklus kezelést

**Várható kimenet:**
```
Diák: Kovács Anna (STU001)
Cím: 123 Fő utca, Budapest, Magyarország, 12345
Teljes cím: 123 Fő utca, Budapest, Magyarország 12345
```

### Fájl elnevezési konvenció:
- Java fájlok: `Subject.java`, `SchoolClass.java`, stb.
- Képernyőképek: `Subject-output.png`, `SchoolClass-output.png`, stb.
- Dokumentáció: `kapcsolat-magyarazatok.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj egyszerű kapcsolatokkal**: Kezdj alapvető kapcsolatokkal
2. **Értsd meg a függetlenséget**: Tudd, mikor létezhetnek objektumok függetlenül
3. **Gyakorold az életciklus kezelést**: Értsd meg az objektumok létrehozását és megsemmisítését
4. **Használj valós példákat**: Gondolj valós kapcsolatokra
5. **Teszteld a kapcsolatokat**: Ellenőrizd, hogy a kapcsolatok megfelelően működnek

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Hibás kapcsolat típus**: Kompozíció használata aggregáció helyett
2. **Körkörös függőségek**: Körkörös hivatkozások létrehozása osztályok között
3. **Szoros csatolás**: Osztályok túl függővé tétele egymástól
4. **Hiányzó null ellenőrzések**: Nem ellenőrzöd a null hivatkozásokat
5. **Rossz életciklus kezelés**: Nem megfelelő objektum létrehozás és megsemmisítés

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett Kapcsolatok
- Implementálj sok-sok kapcsolatokat
- Adj hozzá kapcsolat validációt
- Készíts kapcsolat diagramokat
- Implementálj kapcsolat korlátokat

### Bónusz 2: Kapcsolat Elemzés
- Adj hozzá kapcsolat statisztikákat
- Implementálj kapcsolat lekérdezéseket
- Készíts kapcsolat jelentéseket
- Adj hozzá kapcsolat validációt

### Bónusz 3: Dinamikus Kapcsolatok
- Engedélyezd a dinamikus kapcsolat változásokat
- Implementálj kapcsolat eseményeket
- Adj hozzá kapcsolat értesítéseket
- Készíts kapcsolat előzményeket

---

**Sok sikert az OOP kapcsolatok feladatához! Ne feledd, a jó kapcsolatok teszik jóvá az objektum-orientált tervezést! 🚀**
