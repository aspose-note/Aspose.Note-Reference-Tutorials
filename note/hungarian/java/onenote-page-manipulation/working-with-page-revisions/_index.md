---
date: 2026-01-15
description: Ismerje meg, hogyan követheti nyomon a OneNote változásait, és kezelheti
  az oldalrevíziókat a OneNote dokumentumokban az Aspose.Note for Java segítségével.
  Tartalmaz egy revízióösszegző példát és azt, hogyan módosíthatja a revízió dátumát.
linktitle: Working with Page Revisions in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote változások nyomon követése – Oldalrevíziók kezelése az Aspose.Note
  segítségével
url: /hu/java/onenote-page-manipulation/working-with-page-revisions/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote oldalrevíziók kezelése - Aspose.Note

## Bevezetés

A OneNote egy hatékony eszköz a jegyzetek rendszerezésére, és amikor **track changes onenote**-ra van szükség, az oldalrevíziók kezelése elengedhetetlen a hatékony együttműködéshez. Az Aspose.Note for Java segítségével programozottan kezelheted a revíziókat, megtekintheted, ki szerkesztett egy oldalt, és még az időbélyegeket is módosíthatod. Ez az útmutató végigvezet minden lépésen, a dokumentum betöltésétől a revízióösszefoglaló frissítéséig.

## Gyors válaszok
- **Mit jelent a “track changes onenote”?** Az azt jelenti, hogy nyomon követed, ki szerkesztett egy OneNote oldalt és mikor.
- **Melyik könyvtár szükséges?** Aspose.Note for Java.
- **Módosíthatom a revízió szerzőjét vagy dátumát?** Igen, a RevisionSummary API használatával (`modify revision date`).
- **Szükség van előre egy OneNote fájlra?** Igen, egy mintas `.one` fájl szükséges.
- **Szükséges licenc a termeléshez?** Érvényes Aspose.Note licenc szükséges kereskedelmi használathoz.

## Mi az a revízióösszefoglaló példa?
A *revision summary* metaadatokat biztosít a legutóbbi változásokról egy oldalon – a szerző nevét, az utolsó módosítás időpontját és egyéb részleteket. Ebben az útmutatóban lekérdezzük és megjelenítjük ezeket az információkat, majd megmutatjuk, hogyan **modify revision date**.

## Miért használjunk track changes onenote-t az Aspose.Note-tal?
- **Collaboration:** Gyorsan látható, ki végezte a legújabb szerkesztéseket.
- **Auditing:** Megbízható változástörténetet tart meg a megfelelőség érdekében.
- **Automation:** Integrálja a revíziókezelést a háttérszolgáltatásokba vagy migrációs eszközökbe.

## Előkövetelmények

### Java fejlesztői környezet
Győződj meg róla, hogy a rendszereden telepítve van a Java Development Kit (JDK).

### Aspose.Note for Java könyvtár
Töltsd le és telepítsd az Aspose.Note for Java könyvtárat innen: [here](https://releases.aspose.com/note/java/).

### OneNote dokumentum
Készüljön egy mintas OneNote dokumentum tesztelési célokra.

## Csomagok importálása

A Java projektedben importáld a szükséges csomagokat az Aspose.Note for Java használatához.

```java
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.RevisionSummary;
import java.io.IOException;
import java.util.Calendar;
```

Törjük fel a megadott példát több lépésre a jobb megértés érdekében.

## 1. lépés: OneNote dokumentum betöltése

Először töltsd be a OneNote dokumentumot, és szerezd meg az első gyermekoldalt.

```java
String dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Sample1.one");
Page page = document.getFirstChild();
```

## 2. lépés: Oldal revízióösszefoglaló olvasása

Olvasd be az oldal tartalomrevízió összefoglalóját. Ez a **revision summary example**, amely megmutatja, ki szerkesztette utoljára az oldalt.

```java
RevisionSummary pageRevisionInfo = page.getPageContentRevisionSummary();
System.out.println(String.format("Author:\t%s\nModified:\t%s",
        pageRevisionInfo.getAuthorMostRecent(),
        pageRevisionInfo.getLastModifiedTime().toString()));
```

## 3. lépés: Oldal revízióösszefoglaló frissítése

Frissítsd az oldal revízióösszefoglalóját egy új szerzővel és egy új módosítási dátummal. Ez bemutatja, hogyan **modify revision date** programozottan.

```java
pageRevisionInfo.setAuthorMostRecent("New Author");
Calendar modifiedDate = Calendar.getInstance();
pageRevisionInfo.setLastModifiedTime(modifiedDate.getTime());
document.save(dataDir + "WorkingWithPageRevisions_out.one");
```

## Összegzés

A OneNote dokumentumok oldalrevízióinak programozott kezelése egyszerűsíthető az Aspose.Note for Java segítségével. Az ebben az útmutatóban leírt lépések követésével hatékonyan **track changes onenote**, megtekintheted a revízió részleteit, és akár **modify revision date** is elvégezhető a munkafolyamatodhoz igazítva.

## GYIK

### Q1: Használhatom az Aspose.Note for Java-t más Java könyvtárakkal?
A: Igen, az Aspose.Note for Java integrálható más Java könyvtárakkal a funkcionalitás bővítése érdekében.

### Q2: Támogatja az Aspose.Note for Java az összes OneNote dokumentum verziót?
A: Az Aspose.Note for Java különböző OneNote dokumentum verziókat támogat, beleértve a régebbi verziókat is.

### Q3: Alkalmas-e az Aspose.Note for Java vállalati szintű alkalmazásokhoz?
A: Teljes mértékben, az Aspose.Note for Java úgy lett tervezve, hogy megfeleljen a vállalati szintű alkalmazások igényeinek, robusztus funkciókkal és skálázhatósággal.

### Q4: Testreszabhatom-e az oldalrevíziókat az Aspose.Note for Java-val?
A: Igen, az Aspose.Note for Java segítségével a saját igényeidnek megfelelően testreszabhatod az oldalrevíziókat.

### Q5: Hol kaphatok támogatást az Aspose.Note for Java-hoz?
A: Támogatást az Aspose.Note for Java-hoz a [Aspose.Note fórumon](https://forum.aspose.com/c/note/28) kaphatsz.

---

**Legutóbb frissítve:** 2026-01-15  
**Tesztelt verzió:** Aspose.Note for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}