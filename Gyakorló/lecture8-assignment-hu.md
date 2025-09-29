# 8. Gyakorló Feladat: Kivételkezelés

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni a kivételkezelés fogalmakat, amelyeket a 8. előadásban tanultál. Létrehozol egyedi kivétel osztályokat, implementálsz try-catch blokkokat és gyakorlod a hibakezelés legjobb gyakorlatait.

## 🎯 Tanulási Célok
- Kivétel hierarchia és típusok megértése
- Try-catch-finally blokkok megértése
- Egyedi kivételek létrehozása
- Hibakezelés legjobb gyakorlatainak implementálása
- Különböző kivétel típusok kezelése
- Robusztus hibakezelés tervezése

## 📝 Feladat Feladatok

### Feladat 1: Egyedi Kivétel Létrehozás (30 pont)
Hozz létre egyedi kivétel osztályokat az iskolai rendszerhez:

**Követelmények:**
- **DiákNemTalálhatóKivétel**:
  - Mezők: diákAzonosító, keresésiKritérium
  - Konstruktorok: alapértelmezett, üzenettel, diákAzonosítóval, teljes
  - Metódusok: getDetailedMessage(), getUserFriendlyMessage(), getSuggestions()
- **OsztályTeleKivétel**:
  - Mezők: osztályNév, jelenlegiLétszám, maxKapacitás
  - Konstruktorok: alapértelmezett, üzenettel, osztály információval, teljes
  - Metódusok: getAvailableSpots(), getEnrollmentPercentage(), getSuggestions()
- **ÉrvénytelenAdatKivétel**:
  - Mezők: mezőNév, érvénytelenÉrték, vártFormátum, validációsSzabály
  - Konstruktorok: alapértelmezett, üzenettel, mező információval, teljes
  - Metódusok: getFieldSpecificHelp(), getCorrectedValueSuggestion(), isRecoverable()

**Várható kimenet:**
```
DiákNemTalálhatóKivétel: Diák nem található (Diák Azonosító: STU999, Keresési Kritérium: Azonosító)
Sajnáljuk, nem találtunk diákot 'STU999' azonosítóval. Kérjük, ellenőrizze az információkat és próbálja újra.
Javaslatok:
1. Ellenőrizze, hogy a diák azonosító helyes-e
2. Ellenőrizze, hogy a diák be van-e iratkozva a rendszerbe
3. Próbáljon keresni név szerint azonosító helyett
4. Vegye fel a kapcsolatot az adminisztrátorral, ha a probléma továbbra is fennáll
```

### Feladat 2: Kivételkezelés Implementáció (25 pont)
Implementálj kivételkezelést a DiákMenedzser osztályban:

**Követelmények:**
- **DiákMenedzser metódusok**:
  - addStudent() validációval
  - findStudentById() kivételkezeléssel
  - enrollStudentInClass() kapacitás ellenőrzéssel
  - validateStudentData() mező validációval
- **Kivételkezelés**:
  - Használd a try-catch blokkokat megfelelően
  - Kezeld a specifikus kivételeket
  - Adj értelmes hibaüzeneteket
  - Implementálj hibakezelési stratégiákat

**Várható kimenet:**
```
=== Kivételkezelés Demo ===
Diák hozzáadása: Kovács Anna
Diák sikeresen hozzáadva!

Diák keresése: STU999
Hiba: DiákNemTalálhatóKivétel: Diák nem található (Diák Azonosító: STU999, Keresési Kritérium: Azonosító)
Helyreállítás: Próbálok keresni név szerint helyette...

Diák beiratkozása osztályba: Matematika 101
Hiba: OsztályTeleKivétel: Az osztály maximális kapacitáson van (Osztály: Matematika 101, Létszám: 25/25, 100.0%)
Helyreállítás: Alternatív osztályok javaslása...
```

### Feladat 3: Try-Catch-Finally Blokkok (20 pont)
Gyakorold a try-catch-finally blokkok használatát:

**Követelmények:**
- **Fájl műveletek**:
  - Olvass fájlból kivételkezeléssel
  - Írj fájlba kivételkezeléssel
  - Kezeld a FileNotFoundException-t
  - Kezeld az IOException-t
- **Adat feldolgozás**:
  - Parse-olj adatokat kivételkezeléssel
  - Kezeld a NumberFormatException-t
  - Kezeld az ArrayIndexOutOfBoundsException-t
- **Erőforrás kezelés**:
  - Használd a try-with-resources-t
  - Biztosítsd a megfelelő takarítást
  - Kezeld az erőforrás kivételeket

**Várható kimenet:**
```
=== Try-Catch-Finally Demo ===
Fájl olvasás kísérlet: diákok.txt
Fájl sikeresen elolvasva!
Finally blokk: Fájl műveletek befejezve

Adat parse-olás kísérlet: abc
Hiba: NumberFormatException: A bemeneti sztring: "abc"
Finally blokk: Adat feldolgozás befejezve

Tömb index elérés kísérlet: 10
Hiba: ArrayIndexOutOfBoundsException: Index 10 kívül esik a 5 hosszúságú tömbön
Finally blokk: Tömb műveletek befejezve
```

### Feladat 4: Hibakezelési Stratégiák (25 pont)
Implementálj átfogó hibakezelési stratégiákat:

**Követelmények:**
- **Bemenet validáció**:
  - Validáld a felhasználói bemenetet
  - Kezeld az érvénytelen adatokat
  - Adj javítási javaslatokat
  - Implementálj újrapróbálkozási mechanizmusokat
- **Hibakezelés**:
  - Implementálj tartalék stratégiákat
  - Adj alternatív lehetőségeket
  - Naplózd a hibákat megfelelően
  - Értesítsd a felhasználókat a hibákról
- **Robusztus hibakezelés**:
  - Kezeld a több kivétel típust
  - Implementálj hibakezelési eszkalációt
  - Adj felhasználóbarát üzeneteket
  - Tartsd fenn a rendszer stabilitását

**Várható kimenet:**
```
=== Hibakezelési Stratégiák ===
Bemenet validáció:
Adja meg a diák azonosítót: abc
Hiba: ÉrvénytelenAdatKivétel: Érvénytelen diák azonosító formátum (Mező: diákAzonosító, Érvénytelen Érték: abc, Várt Formátum: STU után 3 számjegy)
Javaslat: Próbálja STU001, STU002, stb.
Újrapróbálkozás: Adja meg a diák azonosítót: STU001
Diák találva: Kovács Anna

Hibakezelés:
Diák keresése: STU999
Hiba: DiákNemTalálhatóKivétel
Helyreállítás: Keresés név szerint helyette...
Diák találva: Nagy Péter (STU002)

Tartalék stratégia:
Elsődleges módszer sikertelen, tartalék használata...
Tartalék sikeres!
```

## 📁 Fájl Struktúra
Hozd létre a következő fájlokat a `lecture8` könyvtárban:
```
src/main/java/lecture8/
├── exceptions/
│   ├── StudentNotFoundException.java
│   ├── ClassFullException.java
│   └── InvalidDataException.java
├── StudentManager.java
├── ExceptionHandlingDemo.java
└── ErrorRecoveryDemo.java
```


### Fájl elnevezési konvenció:
- Java fájlok: `StudentNotFoundException.java`, `StudentManager.java`, stb.
- Képernyőképek: `StudentNotFoundException-output.png`, `StudentManager-output.png`, stb.
- Dokumentáció: `kivetelkezeles-magyarazatok.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj egyszerű kivételekkel**: Kezdj alapvető kivétel típusokkal
2. **Demonstrálj a try-catch-et**: Mutasd meg a kivételkezelés folyamatát
3. **Hozz létre egyedi kivételeket**: Mutasd meg, hogyan hozhatsz létre értelmes kivételeket
4. **Gyakorold a helyreállítást**: Mutasd meg, hogyan lehet helyreállni a hibákból
5. **Emelkedj a legjobb gyakorlatokra**: Taníts megfelelő hibakezelést

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Generikus kivétel kezelés**: Túl széles kivételkezelés
2. **Kivételek figyelmen kívül hagyása**: Nem kezeli a kivételeket megfelelően
3. **Üres catch blokkok**: Nem biztosít kivételkezelést
4. **Rossz hibaüzenetek**: Nem biztosít értelmes hiba információt
5. **Erőforrás szivárgás**: Nem zárja meg megfelelően az erőforrásokat

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett kivételkezelés
- Implementálj kivétel láncolást
- Hozz létre kivétel hierarchiákat
- Implementálj kivétel naplózást
- Adj hozzá kivétel monitorozást

### Bónusz 2: Hibakezelési minták
- Implementálj újrapróbálkozási mintákat
- Hozz létre áramkör megszakító mintákat
- Implementálj tartalék mintákat
- Adj hozzá hibakezelési eszkalációt

### Bónusz 3: Kivétel tesztelés
- Hozz létre kivétel teszt eseteket
- Implementálj kivétel mockolást
- Teszteld a hiba forgatókönyveket
- Validáld a kivételkezelést

---

**Sok sikert a kivételkezelés feladatához! Ne feledd, a jó kivételkezelés teszik a programjaidat robusztus és felhasználóbarát! 🚀**
