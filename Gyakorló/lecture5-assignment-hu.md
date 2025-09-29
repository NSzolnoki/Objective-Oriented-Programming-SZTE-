# 5. Előadás Feladat: Polimorfizmus

## 📋 Feladat Áttekintés
Ez a feladat segít gyakorolni a polimorfizmus fogalmakat, amelyeket az 5. előadásban tanultál. Létrehozol öröklési hierarchiákat, implementálsz metódus felülírásokat és demonstrálod a polimorf viselkedést.

## 🎯 Tanulási Célok
- Öröklés implementáció gyakorlása
- Metódus felülírás megértése
- Polimorf viselkedés gyakorlása
- Super kulcsszó hatékony használata
- Öröklési hierarchiák tervezése
- Polimorf metódus hívások implementálása

## 📝 Feladat Feladatok

### Feladat 1: Személy Hierarchia (30 pont)
Hozz létre egy Személy öröklési hierarchiát a következő osztályokkal:

**Követelmények:**
- **Személy Osztály (Alaposztály)**:
  - Mezők: név, életkor, email, telefonszám, cím
  - Konstruktorok: alapértelmezett, paraméterezett, teljes
  - Metódusok: getterek, setterek, displayInfo(), getRole(), getStatus()
  - Absztrakt metódusok: getRole(), getStatus(), displayInfo()
- **Diák Osztály (extends Személy)**:
  - További mezők: diákazonosító, osztály, átlag, szülő neve
  - Felülírt metódusok: displayInfo(), getRole(), getStatus()
  - További metódusok: getAcademicStatus(), isEligibleForHonors()
- **Tanár Osztály (extends Személy)**:
  - További mezők: tanárAzonosító, tantárgy, tapasztalatÉvek, fizetés
  - Felülírt metódusok: displayInfo(), getRole(), getStatus()
  - További metódusok: getExperienceLevel(), getPerformanceRating()
- **Adminisztrátor Osztály (extends Személy)**:
  - További mezők: adminAzonosító, tanszék, pozíció
  - Felülírt metódusok: displayInfo(), getRole(), getStatus()
  - További metódusok: getDepartment(), getPosition()

**Várható kimenet:**
```
=== Diák Információ ===
Név: Kovács Anna
Életkor: 20
Szerep: Diák
Státusz: Aktív Diák
Diákazonosító: STU001
Osztály: 10. osztály
Átlag: 3.5
========================
```

### Feladat 2: Polimorf Viselkedés (25 pont)
Demonstrálj polimorf viselkedést a Személy hierarchiával:

**Követelmények:**
- **PolimorfizmusDemo Osztály**:
  - Hozz létre Személy objektumok tömbjeit különböző típusokkal
  - Hívd felülírt metódusokat polimorf módon
  - Használd az instanceof operátort objektum típusok ellenőrzéséhez
  - Implementálj dinamikus metódus kiosztást
- **Implementálandó metódusok**:
  - demonstratePolymorphism()
  - demonstrateMethodOverriding()
  - demonstrateRuntimePolymorphism()
  - demonstrateInheritanceBenefits()

**Várható kimenet:**
```
=== POLIMORF VISELKEDÉS ===
Személy 1 szerep: Személy
Személy 2 szerep: Diák
Személy 3 szerep: Tanár

=== METÓDUS FELÜLÍRÁS ===
Személy: Kovács János (30 éves)
Diák: Kovács Anna (STU001) - 10. osztály - Átlag: 3.5
Tanár: Dr. Kovács (TCH001) - Matematika - 15 év tapasztalat
```

### Feladat 3: Super Kulcsszó Használat (20 pont)
Gyakorold a super kulcsszó hatékony használatát:

**Követelmények:**
- **Fejlett Konstruktorok**:
  - Használd a super() hívást szülő konstruktorok hívásához
  - Adj át paramétereket a szülő konstruktoroknak
  - Inicializáld a gyermek-specifikus mezőket
- **Metódus Felülírás**:
  - Használd a super.metódusNév() hívást szülő metódusok hívásához
  - Bővítsd a szülő funkcionalitást
  - Tartsd meg a szülő viselkedést új funkciók hozzáadásával
- **Implementálandó példák**:
  - Diák konstruktor super() hívással
  - Tanár konstruktor super() hívással
  - Felülírt metódusok super metódus hívásokkal

**Várható kimenet:**
```
Diák létrehozva: Kovács Anna (STU001)
Tanár létrehozva: Dr. Kovács (TCH001)
Metódus felülírás példa:
Szülő metódus hívva
Gyermek metódus hívva
```

### Feladat 4: Öröklés Előnyei (25 pont)
Demonstrálj az öröklés előnyeit:

**Követelmények:**
- **Közös Személy Metódusok**:
  - Mind a Diák és Tanár örökli a Személytől
  - Demonstrálj megosztott funkcionalitást
  - Mutasd meg a kód újrafelhasználást
- **Specifikus Metódusok**:
  - Minden osztálynak saját specifikus metódusai vannak
  - Demonstrálj specializációt
  - Mutasd meg a polimorf viselkedést
- **Öröklés Elemzés**:
  - Hasonlítsd össze a kódot öröklés nélkül és örökléssel
  - Mutasd meg az öröklés előnyeit
  - Demonstrálj metódus felülírást

**Várható kimenet:**
```
=== ÖRÖKLÉS ELŐNYEI ===
Diák életkori kategória: Tizenéves
Tanár életkori kategória: Felnőtt
Diák kiskorú: false
Tanár kiskorú: false

Diák-specifikus metódusok:
Akadémiai státusz: Jó
Teljesítmény szint: Átlag feletti
Támogatás szükséges: false

Tanár-specifikus metódusok:
Tapasztalat szint: Tapasztalt
Éves fizetés: $90000.0
Munkaterhelés státusz: Mérsékelt
```

### Fájl elnevezési konvenció:
- Java fájlok: `Person.java`, `Student.java`, stb.
- Képernyőképek: `Person-output.png`, `Student-output.png`, stb.
- Dokumentáció: `orokles-magyarazatok.txt`
- Reflexió: `reflexio.txt`

## 💡 Sikerhez vezető tippek

1. **Kezdj az alaposztállyal**: Hozd létre a Személy osztályt először
2. **Értsd meg az öröklést**: Tudd, mit örökölnek a gyermek osztályok
3. **Gyakorold a felülírást**: Implementálj metódusokat helyesen
4. **Használd a Super kulcsszót**: Hívd szülő metódusokat amikor szükséges
5. **Teszteld a polimorfizmust**: Ellenőrizd, hogy a polimorf viselkedés működik

## 🚨 Gyakori hibák, amelyeket el kell kerülni

1. **Felejtett super()**: Nem hívod a szülő konstruktort
2. **Hibás metódus szignatúra**: Metódus szignatúra megváltoztatása felülíráskor
3. **Hozzáférés módosító problémák**: Felülírt metódus korlátozóbbá tétele
4. **Körkörös öröklés**: Körkörös öröklési láncok létrehozása
5. **Hiányzó @Override**: Nem használod a @Override annotációt

## 🎯 Bónusz kihívások (Opcionális)

### Bónusz 1: Fejlett Öröklés
- Hozz létre mélyebb öröklési hierarchiákat
- Implementálj több szintű öröklést
- Adj hozzá absztrakt metódusokat
- Készíts öröklési diagramokat

### Bónusz 2: Polimorf Gyűjtemények
- Hozz létre Személy objektumok gyűjteményeit
- Implementálj polimorf rendezést
- Adj hozzá polimorf keresést
- Készíts polimorf jelentéseket

### Bónusz 3: Dinamikus Polimorfizmus
- Implementálj dinamikus metódus kiosztást
- Adj hozzá futásidejű típus ellenőrzést
- Hozz létre polimorf gyárakat
- Implementálj polimorf szerializációt

---

**Sok sikert a polimorfizmus feladatához! Ne feledd, az öröklés és polimorfizmus az objektum-orientált programozás alapja! 🚀**
