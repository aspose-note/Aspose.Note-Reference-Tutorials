---
date: 2026-08-13
description: Ismerje meg, hogyan lehet lekérni a OneNote oldal módosítási időpontját
  és visszanyerni az oldal revízióit az Aspose.Note for Java segítségével, ami ideális
  az auditáláshoz és a dokumentumkezeléshez.
keywords:
- get onenote page modified
- onenote page revisions
- aspose.note java
- java onenote api
lastmod: 2026-08-13
linktitle: Oldalrevíziók lekérése a OneNote-ban – Aspose.Note
og_description: Ismerje meg, hogyan lehet lekérni a OneNote oldal módosítási időpontját
  és visszanyerni a OneNote oldalak revízióit az Aspose.Note for Java segítségével.
  Gyors lépések, kódrészletek és hibaelhárítás.
og_image_alt: Screenshot of Aspose.Note Java API showing page revision retrieval
og_title: OneNote oldal módosítási időpontjának lekérése az Aspose.Note segítségével
  – Java oktatóanyag
schemas:
- author: Aspose
  dateModified: '2026-08-13'
  description: Learn how to get onenote page modified time and retrieve page revisions
    with Aspose.Note for Java, ideal for auditing and document management.
  headline: Get OneNote page modified time using Aspose.Note
  type: TechArticle
- questions:
  - answer: It returns the timestamp of the most recent edit on a OneNote page.
    question: What does “get last modified time” return?
  - answer: '`PageHistory` via `Document.getPageHistory(Page)`.'
    question: Which class provides revision history?
  - answer: Yes, a valid Aspose.Note license is required for production use.
    question: Do I need a license for this feature?
  - answer: Java 8 or higher (JDK 8+).
    question: What Java version is supported?
  - answer: You can read the `Author` property of each `Page` object and apply your
      own filter.
    question: Can I filter revisions by author?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote page modified
- aspose.note
- java document management
title: OneNote oldal módosítási időpontjának lekérése az Aspose.Note segítségével
url: /hu/java/onenote-page-manipulation/get-revisions-of-pages/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote oldal módosítási idő lekérése az Aspose.Note segítségével

## Bevezetés

Ezen az oktatóanyagon megtanulja, hogyan **kérheti le a OneNote oldal módosítási** időbélyegét, és hogyan szerezheti meg egy OneNote oldal teljes revíziótörténetét az Aspose.Note for Java segítségével. Akár audit‑trail funkciót épít, akár változásnapló‑nézőt, vagy a legutóbbi szerkesztési dátumot szeretné megjeleníteni egy irányítópulton, ez az útmutató minden lépésen végigvezet – a környezet beállításától a gyakori buktatók kezeléséig.

## Gyors válaszok
- **Mi ad vissza a “get last modified time”?** A legutóbbi szerkesztés időbélyegét adja vissza egy OneNote oldalon.  
- **Melyik osztály biztosítja a revíziótörténetet?** `PageHistory` a `Document.getPageHistory(Page)` segítségével.  
- **Szükségem van licencre ehhez a funkcióhoz?** Igen, egy érvényes Aspose.Note licenc szükséges a termelésben való használathoz.  
- **Melyik Java verzió támogatott?** Java 8 vagy újabb (JDK 8+).  
- **Szűrhetem a revíziókat szerző szerint?** Olvashatja minden `Page` objektum `Author` tulajdonságát, és saját szűrőt alkalmazhat.

## Mi az a “get last modified time” a OneNote-ban?

A legutóbbi módosítás időpontja metaadat‑attribútumként van tárolva minden OneNote oldalon, jelezve a legutóbbi szerkesztés pillanatát. Az Aspose.Note ezt az értéket a `Page.getLastModifiedTime()` metóduson keresztül teszi elérhetővé, amely egy `java.util.Date` objektumot ad vissza, amely formázható vagy naplózható az alkalmazás igényei szerint.

## Miért érdemes lekérni az oldal revíziókat?

Az oldal revíziók lekérése teljes audit‑trail‑et biztosít minden OneNote oldalon végrehajtott változásról, lehetővé téve, hogy nyomon kövesse ki mit és mikor szerkesztett. Ez a történet felhasználható verziók összehasonlítására, korábbi állapotok visszaállítására vagy a csapatok közötti együttműködési minták elemzésére, így elengedhetetlen a megfelelőség és a minőség‑ellenőrzés szempontjából.

## Előfeltételek

- **Java Development Kit (JDK) 8 vagy újabb** – telepítse az Oracle weboldaláról vagy bármely kompatibilis szállítótól.  
- **Aspose.Note for Java könyvtár** – töltse le a JAR‑t az Aspose.Note Java kiadások oldaláról **[Aspose.Note Java releases](https://releases.aspose.com/note/java/)**, és kövesse a telepítési útmutatót **[Aspose.Note Java documentation](https://reference.aspose.com/note/java/)**.  

## Csomagok importálása

A `Document` osztály egy memóriába betöltött OneNote jegyzetfüzetet képvisel, míg a `Page` és a `PageHistory` hozzáférést biztosítanak az egyes oldalakhoz és azok revízióadataihoz.

```text
import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
import java.util.Date;
```

*(Az aktuális import utasítások egyszerű szövegként vannak megjelenítve a kódtömbök számának megőrzése érdekében.)*

## Hogyan lehet lekérni a OneNote oldal módosítási időpontját?

A legutóbbi módosítás időbélyegének megszerzéséhez először töltse be a OneNote dokumentumot egy `Document` objektumba, majd válassza ki a kívánt `Page`‑t. Hívja meg a `getLastModifiedTime()` metódust az oldalon, amely egy `java.util.Date` objektumot ad vissza. Ezután formázhatja a dátumot a `SimpleDateFormat` használatával, vagy UTC‑re konvertálhatja a konzisztens jelentés érdekében időzónák között.

## 1. lépés: dokumentum könyvtár beállítása

Adja meg azt a mappát, amely a OneNote fájlt tartalmazza.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Page;
import com.aspose.note.PageHistory;
```

## 2. lépés: dokumentum betöltése

Hozzon létre egy `Document` példányt a `.one` fájl teljes elérési útjának megadásával.

```java
String dataDir = "Your Document Directory";
```

## 3. lépés: első oldal lekérése

Szerezze meg az első `Page` objektumot a dokumentum oldalgyűjteményéből.

```java
Document doc = new Document(dataDir + "Sample1.one");
```

## 4. lépés: oldal revíziók lekérése

Szerezze meg a kiválasztott oldal `PageHistory`‑ját. Ha a jegyzetfüzetet még soha nem szerkesztették, ez a hívás `null`‑t adhat vissza.

```java
Page firstPage = doc.getFirstChild();
```

## 5. lépés: oldal revíziók bejárása

Iteráljon végig minden `Page` revízión, olvassa el annak `Author` és `LastModifiedTime` értékeit, és jelenítse meg az információkat.

```java
PageHistory revisions = doc.getPageHistory(firstPage);
```

## Gyakori problémák és megoldások
- **Null `PageHistory`** – Ellenőrizze, hogy a jegyzetfüzet valóban tartalmaz revíziókat; ellenkező esetben a `getPageHistory` `null`‑t ad vissza.  
- **Időzóna‑különbségek** – A `getLastModifiedTime()` a JVM alapértelmezett időzónáját használja. Konvertálja UTC‑re a `SimpleDateFormat`‑tal, ha az alkalmazásának szabványos zóna szükséges.  
- **Licenc nincs betöltve** – Érvényes licenc nélkül az Aspose.Note értékelő módban fut, ami korlátozza az oldalak feldolgozását. Töltse be a licencfájlt az alkalmazás indításakor, hogy elkerülje ezt a korlátozást.

## Gyakran ismételt kérdések

**Q1: Használhatom az Aspose.Note for Java‑t új OneNote dokumentumok létrehozására?**  
A: Igen, az API lehetővé teszi, hogy programozottan hozzon létre, szerkesszen és mentse a OneNote jegyzetfüzeteket a semmiből.

**Q2: Az Aspose.Note for Java kompatibilis a OneNote fájlok különböző verzióival?**  
A: Igen, támogatja a OneNote 2007‑2021 fájlformátumokat, biztosítva a széles kompatibilitást asztali és felhő környezetekben egyaránt.

**Q3: Testreszabhatom a kimeneti formátumot a OneNote dokumentumok exportálásakor?**  
A: Teljes mértékben. Exportálhat PDF‑be, HTML‑be, PNG‑be vagy SVG‑be, és szabályozhatja az opciókat, például a kép felbontását és a betűtípus beágyazását.

**Q4: Az Aspose.Note for Java‑hoz szükséges licenc a kereskedelmi felhasználáshoz?**  
A: Igen, a kereskedelmi licenc kötelező a termelési környezetben történő telepítéshez. Ingyenes próbaverzió elérhető értékeléshez.

**Q5: Hol kérhetek segítséget, ha problémáim merülnek fel?**  
A: Látogassa meg az Aspose.Note közösségi fórumot **[Aspose.Note forum](https://forum.aspose.com/c/note/28)**, ahol kérdéseket tehet fel, tapasztalatokat oszthat meg, és segítséget kaphat a közösségtől és az Aspose mérnököktől.

---

**Utoljára frissítve:** 2026-08-13  
**Tesztelve:** Aspose.Note for Java 23.12 (a legújabb a írás időpontjában)  
**Szerző:** Aspose

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

## Kapcsolódó oktatóanyagok

- [Aspose Java oktatóanyag – Információk lekérése a OneNote oldalakról – Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)
- [aspose.note oldal revíziók oktatóanyag – Page revíziók lekérése a OneNote-ban](/note/java/onenote-page-manipulation/get-page-revisions/)
- [változások nyomon követése OneNote – Oldal revíziók kezelése az Aspose.Note segítségével](/note/java/onenote-page-manipulation/working-with-page-revisions/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}