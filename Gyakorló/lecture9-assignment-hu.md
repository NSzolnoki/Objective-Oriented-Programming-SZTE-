# 9. Gyakorló Feladatsor: Fájlkezelés

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni a fájlkezelés fogalmakat, amelyeket a 9. előadásban tanultál. Implementálsz fájl I/O műveleteket, adatmegőrzést és fájlkezelési rendszereket.

## 🎯 Tanulási Célok
- Fájl I/O műveletek gyakorlása
- Megtanulni a fájlokból való olvasást és fájlokba való írást
- Adatmegőrzés implementálása
- Fájl validáció és hibakezelés gyakorlása
- Adat biztonsági mentés és helyreállítás rendszerek létrehozása
- Különböző fájl formátumokkal dolgozni

## 📝 Feladat Feladatok

### Feladat 1: Fájl Menedzser Implementáció (30 pont)
Hozz létre egy átfogó FájlMenedzser osztályt fájl műveletekhez:

**Követelmények:**
- **Fájl műveletek**:
  - readTextFile(String filename)
  - writeTextFile(String filename, String content)
  - appendToFile(String filename, String content)
  - readLinesFromFile(String filename)
  - writeLinesToFile(String filename, List<String> lines)
- **Fájl kezelés**:
  - fileExists(String filename)
  - getFileSize(String filename)
  - getFileLastModified(String filename)
  - deleteFile(String filename)
  - copyFile(String source, String destination)
- **Könyvtár műveletek**:
  - createDirectory(String directoryName)
  - listFiles(String directory)
  - getFileInfo(String filename)

**Várható kimenet:**
```
=== Fájl Menedzser Demo ===
Fájl Menedzser inicializálva:
- Adat könyvtár: data
- Biztonsági mentés könyvtár: data/backup

Fájl olvasás: diákok.txt
Fájl tartalom:
Kovács Anna,20,anna@email.com,STU001,10. osztály,3.5
Nagy Péter,19,peter@email.com,STU002,9. osztály,3.8

Fájl írás: kimenet.txt
Fájl sikeresen kiírva!

Fájl információ:
Fájl: diákok.txt
Méret: 156 bájt
Utolsó módosítás: 2024-01-15T10:30:00
```

### Feladat 2: Adatmegőrzés Rendszer (25 pont)
Implementálj egy adatmegőrzés rendszert diák adatokhoz:

**Követelmények:**
- **Adat mentés**:
  - saveStudentData(List<Student> students)
  - saveDataToCsv(List<Student> students)
  - saveDataToJson(List<Student> students)
  - createDataBackup(List<Student> students)
- **Adat betöltés**:
  - loadStudentData()
  - loadDataFromCsv()
  - loadDataFromJson()
  - loadDataFromBackup(String backupFile)
- **Adat validáció**:
  - validateDataFormat(String data)
  - checkDataIntegrity(List<Student> students)
  - handleCorruptedData()

**Várható kimenet:**
```
=== Adatmegőrzés Demo ===
Diák adatok mentése fájlba...
Diák adatok sikeresen mentve!

Adatok mentése CSV formátumba...
CSV adatok sikeresen mentve!

Adat biztonsági mentés létrehozása...
Biztonsági mentés létrehozva: backup_20240115_103000.txt

Diák adatok betöltése fájlból...
Betöltve 3 diák a fájlból:
1. Kovács Anna (STU001) - 10. osztály - Átlag: 3.5
2. Nagy Péter (STU002) - 9. osztály - Átlag: 3.8
3. Szabó Mária (STU003) - 11. osztály - Átlag: 3.2
```

### Feladat 3: Konfiguráció Kezelés (20 pont)
Hozz létre egy konfiguráció kezelési rendszert:

**Követelmények:**
- **KonfigurációFájl Osztály**:
  - loadConfiguration(String filename)
  - saveConfiguration(String filename)
  - getConfigValue(String key)
  - setConfigValue(String key, String value)
  - getIntConfigValue(String key, int defaultValue)
  - getBooleanConfigValue(String key, boolean defaultValue)
- **Alapértelmezett konfiguráció**:
  - school.name
  - max.students
  - max.classes
  - data.directory
  - backup.enabled
- **Konfiguráció validáció**:
  - validateConfiguration()
  - checkRequiredSettings()
  - provideDefaultValues()

**Várható kimenet:**
```
=== Konfiguráció Kezelés Demo ===
Konfiguráció betöltése innen: config.properties
Konfiguráció sikeresen betöltve!

Konfiguráció értékek:
- Iskola neve: Általános Iskola
- Max diákok: 100
- Max osztályok: 10
- Adat könyvtár: data
- Biztonsági mentés engedélyezve: true

Konfiguráció mentése...
Konfiguráció sikeresen mentve!
```

### Feladat 4: Fájlkezelés Hibakezeléssel (25 pont)
Implementálj robusztus fájlkezelést hibakezeléssel:

**Követelmények:**
- **Hibakezelés**:
  - Kezeld a FileNotFoundException-t
  - Kezeld az IOException-t
  - Kezeld a SecurityException-t
  - Kezeld az IllegalArgumentException-t
- **Hibakezelés**:
  - Próbáld újra a sikertelen műveleteket
  - Adj tartalék lehetőségeket
  - Hozz létre biztonsági mentés fájlokat
  - Értesítsd a felhasználókat a hibákról
- **Fájl validáció**:
  - Validáld a fájl útvonalakat
  - Ellenőrizd a fájl jogosultságokat
  - Verifikáld a fájl formátumokat
  - Kezeld a sérült fájlokat

**Várható kimenet:**
```
=== Fájlkezelés Hibakezeléssel Demo ===
Fájl olvasás kísérlet: nemlétező.txt
Hiba: FileNotFoundException: nemlétező.txt (Nincs ilyen fájl vagy könyvtár)
Helyreállítás: Alapértelmezett fájl létrehozása...
Alapértelmezett fájl sikeresen létrehozva!

Írás kísérlet védett fájlba: system.txt
Hiba: SecurityException: Hozzáférés megtagadva
Helyreállítás: Felhasználó könyvtárba írás helyette...
Fájl kiírva ide: user/system.txt

Sérült fájl olvasás kísérlet: sérült.txt
Hiba: IOException: A fájl sérültnek tűnik
Helyreállítás: Fájl javítás kísérlet...
Fájl javítás sikertelen. Biztonsági mentés fájl használata...
Biztonsági mentés fájl sikeresen betöltve!
```

## 📁 Fájl Struktúra
Hozd létre a következő fájlokat a `lecture9` könyvtárban:
```
src/main/java/lecture9/
├── FileManager.java
├── DataPersistence.java
├── ConfigurationManager.java
├── FileHandlingDemo.java
└── Student.java (ha még nem létezik)
```

### Fájl elnevezési konvenció:
- Java fájlok: `FileManager.java`, `DataPersistence.java`, stb.
- Adat fájlok: `diákok.txt`, `config.properties`, `backup.txt`
- Képernyőképek: `FileManager-output.png`, `DataPersistence-output.png`, stb.
- Dokumentáció: `fajlkezeles-magyarazatok.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj egyszerű műveletekkel**: Kezdj alapvető fájl olvasás/írás műveletekkel
2. **Használj Try-With-Resources**: Mindig használj try-with-resources fájl műveletekhez
3. **Kezeld a kivételeket**: Implementálj megfelelő kivételkezelést
4. **Tesztelj valós fájlokkal**: Hozz létre minta fájlokat teszteléshez
5. **Validáld az adatokat**: Mindig validáld az adatokat mentés/betöltés előtt

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Fájlok nem zárása**: Fájl stream-ek bezárásának elfelejtése
2. **Rossz hibakezelés**: Nem kezeli a fájl kivételeket megfelelően
3. **Rögzített útvonalak**: Rögzített fájl útvonalak használata
4. **Nincs validáció**: Nem validálja a fájl létezését vagy jogosultságokat
5. **Erőforrás szivárgás**: Nem használja a try-with-resources-t

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett Fájl Műveletek
- Implementálj fájl titkosítás/visszafejtés
- Hozz létre fájl tömörítés/kibontás
- Adj hozzá fájl szinkronizálást
- Implementálj fájl verziókezelést

### Bónusz 2: Adat Formátum Támogatás
- Adj hozzá XML fájl támogatást
- Implementálj JSON fájl kezelést
- Hozz létre egyedi adat formátumokat
- Adj hozzá adat validációs sémákat

### Bónusz 3: Fájlrendszer Integráció
- Implementálj fájlrendszer monitorozást
- Adj hozzá fájl változás észlelést
- Hozz létre fájl szinkronizálást
- Implementálj fájl biztonsági mentés automatizálást

---

**Sok sikert a fájlkezelés feladatához! Ne feledd, a fájlkezelés elengedhetetlen a tartós alkalmazások létrehozásához! 🚀**
