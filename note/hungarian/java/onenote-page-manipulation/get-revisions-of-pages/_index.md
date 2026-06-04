---
date: 2026-01-10
description: Tanulja meg, hogyan lehet lekérni az utolsó módosítás időpontját és a
  OneNote‑oldalak revízióit az Aspose.Note for Java segítségével. Integrálja ezt Java‑alkalmazásaiba
  a hatékony dokumentumkezelés érdekében.
linktitle: Get Revisions of Pages in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Hogyan lehet lekérdezni a OneNote oldalak legutóbbi módosítási idejét – Aspose.Note
url: /hu/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oldalak revízióinak lekérése a OneNote-ban – Aspose.Note

## Bevezetés

Ebben az útmutatóban **az utolsó módosítás időpontját** fogod lekérni a OneNote-dokumentum oldalaiból, és megismerheted, hogyan lehet a teljes revíziótörténetet lekérni az Aspose.Note for Java segítségével. Akár dokumentumkezelő rendszert építesz, változásokat auditálsz, vagy egyszerűen csak meg szeretnéd jeleníteni, mikor szerkesztették utoljára az oldalt, ez az útmutató pontosan megmutatja, hogyan lehet ezt az információt programozottan kinyerni.

## Gyors válaszok
- **Mit ad vissza a “get last modified time”?** A legutóbbi szerkesztés időbélyegét egy OneNote oldalról.  
- **Melyik osztály biztosítja a revíziótörténetet?** `PageHistory` a `Document.getPageHistory(Page)` segítségével.  
- **Szükség van licencre ehhez a funkcióhoz?** Igen, érvényes Aspose.Note licenc szükséges a termelésben való használathoz.  
- **Melyik Java verzió támogatott?** Java 8 vagy újabb (JDK 8+).  
- **Szűrhetem a revíziókat szerző szerint?** Olvashatod az egyes `Page` objektumok `Author` tulajdonságát, és saját szűrőt alkalmazhatsz.

## Mi az a “get last modified time” a OneNote-ban?

A **last modified time** egy metaadat‑mező, amely minden oldalhoz tárolja, mikor történt a legutóbbi módosítás. Az Aspose.Note ezt az értéket a `Page.getLastModifiedTime()` metóduson keresztül teszi elérhetővé, így könnyen megjeleníthető vagy naplózható a változások dátuma.

## Miért érdemes lekérni az oldal revíziókat?

- **Audit nyomvonalak:** Rögzítsd, ki mit és mikor változtatott.  
- **Verzió összehasonlítás:** Készíts olyan funkciókat, amelyek két revíziót egymás mellé helyeznek.  
- **Felhasználói együttműködés elemzése:** Értsd meg a szerkesztési mintákat a megosztott jegyzetfüzetekben.  

## Előfeltételek

Mielőtt elkezdenéd, győződj meg róla, hogy a következőkkel rendelkezel:

### Java Development Kit (JDK) telepítése
Telepítsd a JDK 8 vagy újabb verzióját az Oracle weboldaláról vagy a kedvenc csomagkezelődből.

### Aspose.Note for Java könyvtár
Töltsd le a könyvtárat a hivatalos oldalról. A letöltési hivatkozást **[itt](https://releases.aspose.com/note/java/)** találod. Kövesd a telepítési útmutatót a dokumentációban **[itt](https://reference.aspose.com/note/java/)**.

## Csomagok importálása

A kezdéshez importáld a szükséges csomagokat a Java projektedbe. Ezek a csomagok lehetővé teszik, hogy kihasználhasd az Aspose.Note for Java által nyújtott funkcionalitást.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

Most bontsuk le a példakódot több lépésre, hogy megértsük az egyes komponensek szerepét és működését.

## Hogyan kérjük le egy OneNote oldal utolsó módosítási időpontját

### 1. lépés: Dokumentum könyvtár beállítása
Határozd meg azt a könyvtárat, ahol a OneNote dokumentumod található.

```java
String dataDir = "Your Document Directory";
```

### 2. lépés: Dokumentum betöltése
Töltsd be a OneNote dokumentumot az Aspose.Note-ba.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

### 3. lépés: Első oldal lekérése
Szerezd meg a dokumentum első oldalát.

```java
Page firstPage = doc.getFirstChild();
```

### 4. lépés: Oldal revíziók lekérése
Szerezd be az oldal revíziótörténetét.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

### 5. lépés: Oldal revíziók bejárása
Iteráld végig az oldal revízióinak listáját, és olvasd ki a releváns információkat, beleértve a **last modified time** értéket is.

```java
for (Page pageRevision : revisions) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

## Gyakori problémák és megoldások
- **Null `PageHistory`:** Győződj meg róla, hogy a dokumentum valóban tartalmaz revíziókat; ellenkező esetben a `getPageHistory` `null`‑t adhat vissza.  
- **Időzóna‑eltérések:** A `getLastModifiedTime()` egy `java.util.Date` objektumot ad vissza a rendszer alapértelmezett időzónájában. Szükség esetén konvertáld UTC‑re.  
- **Licenc nincs betöltve:** Érvényes licenc hiányában az Aspose.Note értékelő módban működik, ami korlátozhatja a feldolgozott oldalak számát.

## Gyakran ismételt kérdések

### Q1: Használhatom az Aspose.Note for Java‑t új OneNote dokumentumok létrehozására?
**A1:** Igen, az Aspose.Note for Java átfogó támogatást nyújt OneNote dokumentumok programozott létrehozásához, olvasásához és módosításához.

### Q2: Kompatibilis-e az Aspose.Note for Java különböző OneNote fájlverziókkal?
**A2:** Igen, az Aspose.Note for Java számos Microsoft OneNote fájlverziót támogat, így biztosítva a kompatibilitást különböző környezetekben.

### Q3: Testreszabhatom-e a kimeneti formátumot OneNote dokumentumok exportálásakor?
**A3:** Teljes mértékben, az Aspose.Note for Java rugalmas exportálási lehetőségeket kínál PDF, HTML és képek formátumokba, testreszabható beállításokkal.

### Q4: Szükséges-e licenc a kereskedelmi felhasználáshoz?
**A4:** Igen, kereskedelmi felhasználáshoz érvényes licenc szükséges az Aspose.Note for Java‑hoz. Licencet a Aspose weboldaláról szerezhetsz be.

### Q5: Hol kaphatok segítséget, ha problémáim vannak vagy kérdéseim merülnek fel az Aspose.Note for Java‑val kapcsolatban?
**A5:** Támogatásért és segítségért látogass el az Aspose.Note fórumra **[itt](https://forum.aspose.com/c/note/28)**, ahol kérdéseket tehetsz fel, tapasztalatokat oszthatsz meg, és más felhasználókkal, szakértőkkel léphetsz kapcsolatba.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.Note for Java 23.12 (legújabb a kiadás időpontjában)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}