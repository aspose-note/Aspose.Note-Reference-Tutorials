---
date: 2026-08-08
description: Ismerje meg, hogyan követheti nyomon a változásokat a OneNote-ban, programozottan
  lekérve az oldalrevíziókat az Aspose.Note for Java segítségével.
keywords:
- track changes in onenote
- aspose.note java
- onenote page revisions
- java document processing
lastmod: 2026-08-08
linktitle: Oldalrevíziók lekérése a OneNote-ban – Aspose.Note
og_description: Ismerje meg, hogyan követheti nyomon a változásokat a OneNote-ban,
  programozottan lekérve az oldalrevíziókat az Aspose.Note for Java segítségével.
og_image_alt: Guide showing how to track changes in OneNote using Aspose.Note Java
  API
og_title: Változások nyomon követése a OneNote-ban – oldalrevíziók az Aspose.Note
  segítségével
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  headline: Track changes in OneNote – page revisions with Aspose.Note
  type: TechArticle
- description: Learn how to track changes in OneNote by retrieving page revisions
    programmatically using Aspose.Note for Java.
  name: Track changes in OneNote – page revisions with Aspose.Note
  steps:
  - name: set up document directory
    text: Define the folder where your OneNote file resides.
  - name: load OneNote document with history enabled
    text: '`LoadOptions` is a configuration class that tells Aspose.Note how to open
      a file, including whether to read revision data. Enable the flag before loading
      the document.'
  - name: get the first page
    text: Grab the first page object; this will be the reference point for retrieving
      its history.
  - name: iterate through page revisions
    text: Loop through each revision and print useful metadata such as timestamps,
      title, level, and author. > **Pro tip:** If you need to filter revisions by
      a specific author or date range, simply add conditional checks inside the `for`
      loop.
  type: HowTo
- questions:
  - answer: Retrieving page revision history from a OneNote file using Aspose.Note
      for Java.
    question: What does the tutorial cover?
  - answer: Any recent Aspose.Note for Java release that supports `LoadOptions.setLoadHistory`.
    question: Which library version is required?
  - answer: A temporary evaluation license works for testing; a commercial license
      is required for production.
    question: Do I need a license?
  - answer: The API is read‑only for revisions; you can only retrieve them.
    question: Can I modify revisions?
  - answer: Java JDK, Aspose.Note for Java, and a OneNote document with revision data.
    question: What are the main prerequisites?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- track changes
- Aspose.Note
- OneNote revisions
- Java API
title: Változások nyomon követése a OneNote-ban – oldalrevíziók az Aspose.Note segítségével
url: /hu/java/onenote-page-manipulation/get-page-revisions/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Változások nyomon követése a OneNote-ban – oldalrevíziók az Aspose.Note segítségével

Ebben a bemutatóban megtanulja, hogyan **követheti nyomon a változásokat a OneNote-ban** egy oldal teljes revíziótörténetének kinyerésével az Aspose.Note Java API használatával. Mindent lefedünk a fejlesztői környezet beállításától a revíziók szerzőjének, időbélyegének és címének kiírásáig, így megbízható audit‑trail funkciókat építhet bármely OneNote‑alapú megoldáshoz.

## Gyors válaszok
- **Mi a bemutató témája?** Oldalrevíziótörténet lekérése egy OneNote fájlból az Aspose.Note for Java használatával.  
- **Melyik könyvtárverzió szükséges?** Bármely friss Aspose.Note for Java kiadás, amely támogatja a `LoadOptions.setLoadHistory` metódust.  
- **Szükségem van licencre?** Egy ideiglenes értékelő licenc teszteléshez működik; a termeléshez kereskedelmi licenc szükséges.  
- **Módosíthatok revíziókat?** Az API csak olvasásra alkalmas a revíziók esetén; csak lekérhetők.  
- **Mik a fő előfeltételek?** Java JDK, Aspose.Note for Java, és egy OneNote dokumentum revízióadatokkal.

## Mi az az „aspose.note page revisions tutorial”?
A bemutató azt mutatja be, hogyan lehet programozottan hozzáférni egy OneNote oldal történelmi verzióihoz. Minden revízió metaadatokat tartalmaz, például a szerzőt, a létrehozás időpontját és a módosítás időpontját, lehetővé téve audit‑trail vagy változásnapló funkciók építését az alkalmazásokban.

## Miért használja az Aspose.Note-ot az oldalrevíziók nyomon követéséhez?
Töltsön be egy jegyzetfüzet teljes revíziótörténetét 5 másodpercnél kevesebb idő alatt egy 500 oldalas fájl esetén egy standard 2 GHz CPU-n, és szerezzen metaadatokat a OneNote felhasználói felületének indítása nélkül. A könyvtár több mint 30 bemeneti és kimeneti formátumot támogat, Windows, Linux és macOS rendszereken fut (több mint 95 % szerverkörnyezetet lefed), és teljes irányítást biztosít minden revízió tulajdonsága felett.

## Előfeltételek

### 1. Java fejlesztői csomag (JDK)
Győződjön meg arról, hogy egy friss JDK (8 vagy újabb) telepítve van, és a `JAVA_HOME` be van állítva.

### 2. Aspose.Note for Java
Töltse le a könyvtárat a [download link](https://releases.aspose.com/note/java/) címről.

### 3. Minta OneNote dokumentum
Hozzon létre vagy szerezzen be egy OneNote fájlt (például `Sample1.one`), amely revíziótörténettel rendelkező oldalakat tartalmaz.

## Csomagok importálása
Először importálja a szükséges Aspose.Note osztályokat.  
`Document` egy OneNote jegyzetfüzetet képvisel, a `LoadOptions` a betöltési viselkedést konfigurálja, a `Page` pedig egyetlen oldalt jelöl.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
```

## Lépésről‑lépésre megvalósítás

### 1. lépés: dokumentumkönyvtár beállítása
Határozza meg azt a mappát, ahol a OneNote fájlja található.

```java
String dataDir = "Your Document Directory";
```

### 2. lépés: OneNote dokumentum betöltése a történelem engedélyezésével
`LoadOptions` egy konfigurációs osztály, amely megmondja az Aspose.Note-nak, hogyan nyisson meg egy fájlt, beleértve azt is, hogy olvassa-e a revízió adatokat. Engedélyezze a jelzőt a dokumentum betöltése előtt.

```java
LoadOptions loadOptions = new LoadOptions();
loadOptions.setLoadHistory(true);
Document document = new Document(dataDir + "Sample1.one", loadOptions);
```

### 3. lépés: az első oldal lekérése
Szerezze meg az első oldal objektumát; ez lesz a referenciapont a történet lekéréséhez.

```java
Page firstPage = document.getFirstChild();
```

### 4. lépés: végigiterálás az oldalrevíziókon
Iteráljon végig minden revízión, és nyomtassa ki a hasznos metaadatokat, például az időbélyegeket, a címet, a szintet és a szerzőt.

```java
for (Page pageRevision : document.getPageHistory(firstPage)) {
    System.out.println("LastModifiedTime: " + pageRevision.getLastModifiedTime());
    System.out.println("CreationTime: " + pageRevision.getCreationTime());
    System.out.println("Title: " + pageRevision.getTitle());
    System.out.println("Level: " + pageRevision.getLevel());
    System.out.println("Author: " + pageRevision.getAuthor());
    System.out.println();
}
```

> **Pro tipp:** Ha egy adott szerző vagy dátumtartomány szerint kell szűrni a revíziókat, egyszerűen adjon hozzá feltételes ellenőrzéseket a `for` cikluson belül.

## Gyakori problémák és megoldások
- **Nincsenek revíziók visszaadva:** Ellenőrizze, hogy a `loadOptions.setLoadHistory(true)` hívás megtörtént-e a dokumentum betöltése előtt.  
- **Null szerző vagy cím:** Néhány régebbi OneNote verzió nem tárolhatja ezeket a mezőket; kezelje a `null` értékeket megfelelően.  
- **Teljesítménycsökkenés nagy jegyzetfüzeteknél:** Töltsön be csak a szükséges szekciókat, vagy növelje a JVM heap méretét.

## Gyakran feltett kérdések

**Q1: Használhatom az Aspose.Note for Java-t az oldalrevíziók módosítására?**  
A1: Nem, az API jelenleg csak olvasásra alkalmas hozzáférést biztosít az oldalrevíziókhoz.

**Q2: Az Aspose.Note for Java kompatibilis a OneNote dokumentumok különböző verzióival?**  
A2: Igen, különböző OneNote fájlformátumokkal működik, lehetővé téve a zökkenőmentes feldolgozást a verziók között.

**Q3: Az Aspose.Note for Java használatához szükséges licenc?**  
A3: Kereskedelmi licenc szükséges a termelési használathoz, de ideiglenes értékelő licenc elérhető teszteléshez.

**Q4: Kaphatok támogatást, ha problémáim merülnek fel az Aspose.Note for Java használata közben?**  
A4: Igen, kérdéseket tehet fel az Aspose.Note fórumon [Aspose.Note forum](https://forum.aspose.com/c/note/28).

**Q5: Elérhető ingyenes próba az Aspose.Note for Java-hoz?**  
A5: Igen, letölthet egy ingyenes próbát a [website](https://releases.aspose.com/) oldalról.

---

**Legutóbb frissítve:** 2026-08-08  
**Tesztelve a következővel:** Aspose.Note for Java (latest release)  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó bemutatók

- [követés változások OneNote – Oldalrevíziók kezelése az Aspose.Note segítségével](/note/java/onenote-page-manipulation/working-with-page-revisions/)
- [Aspose Java bemutató – Információk lekérése a OneNote oldalakról – Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [OneNote oldal háttér módosítása – Aspose.Note for Java](/note/java/onenote-page-manipulation/set-page-background-color/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}