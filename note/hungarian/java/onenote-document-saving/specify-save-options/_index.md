---
title: Adja meg a mentési beállításokat a OneNote-ban – Aspose.Note
linktitle: Adja meg a mentési beállításokat a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan adhat meg mentési beállításokat a OneNote-ban az Aspose.Note for Java használatával. Könnyedén testreszabhatja az oldalindex, a számlálás és a tömörítés beállításait.
weight: 24
url: /hu/java/onenote-document-saving/specify-save-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adja meg a mentési beállításokat a OneNote-ban – Aspose.Note

## Bevezetés

Ebből az oktatóanyagból megtudhatja, hogyan adhat meg mentési beállításokat a OneNote-ban az Aspose.Note for Java használatával. Az Aspose.Note egy hatékony Java-könyvtár, amely lehetővé teszi a fejlesztők számára a OneNote-dokumentumok programozott létrehozását, kezelését és konvertálását. Az Aspose.Note segítségével könnyedén vezérelheti a különféle mentési beállításokat, hogy igényei szerint testreszabhassa a kimenetet.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Java programozási nyelv alapismerete.
2. JDK (Java Development Kit) telepítve van a rendszerére.
3.  Aspose.Note for Java könyvtár telepítve. Letöltheti innen[itt](https://releases.aspose.com/note/java/).

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat a Java kódba:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfImageCompression;
import com.aspose.note.PdfSaveOptions;
import java.io.IOException;
```

Bontsuk fel a példát több lépésre:

## 1. lépés: Töltse be a OneNote-dokumentumot

```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory";

// Töltse be a dokumentumot az Aspose.Note-ba.
Document doc = new Document(dataDir + "Aspose.one");
```

 Ebben a lépésben megadjuk a OneNote-dokumentum elérési útját, és betöltjük a dokumentumba`Document` tárgy.

## 2. lépés: Inicializálja a PdfSaveOptions objektumot

```java
// Inicializálja a PdfSaveOptions objektumot
PdfSaveOptions opts = new PdfSaveOptions();
```

 Itt inicializáljuk a`PdfSaveOptions` objektum, amely a dokumentum PDF formátumban történő mentésére vonatkozó beállítások megadására szolgál.

## 3. lépés: Állítsa be az oldalindexet és a számlálást

```java
// Oldalindex beállítása
opts.setPageIndex(2);

// Oldalszám beállítása
opts.setPageCount(3);
```

Ezek a sorok állítják be a mentendő oldalak indexét és számát. Ebben a példában a 2. indextől kezdve összesen 3 oldalt mentünk el.

## 4. lépés: Adja meg a tömörítési beállításokat

```java
// Adja meg a tömörítést, ha szükséges
opts.setImageCompression(PdfImageCompression.Jpeg);
opts.setJpegQuality(90);
```

Itt adjuk meg a PDF képtömörítési beállításait. A tömörítést JPEG formátumra állítottuk, és a JPEG minőséget 90%-ban adjuk meg.

## 5. lépés: Mentse el a dokumentumot a beállításokkal

```java
dataDir = dataDir + "Document.SaveWithOptions_out.pdf";
doc.save(dataDir, opts);
```

Végül elmentjük a dokumentumot a megadott opciókkal. A kimeneti PDF mentésre kerül a megadott helyen a megadott opciókkal.

## Következtetés

Ebben az oktatóanyagban megtanultuk, hogyan adhat meg mentési beállításokat a OneNote-ban az Aspose.Note for Java használatával. A mentési beállítások testreszabásával szabályozhatja a kimeneti dokumentum különböző aspektusait, például az oldalindexet, a számlálást és a tömörítési beállításokat.

## GYIK

### 1. kérdés: Az Aspose.Note képes kezelni a nagy OneNote dokumentumokat?

1. válasz: Igen, az Aspose.Note a nagy OneNote-dokumentumok hatékony kezelésére készült.

### 2. kérdés: Az Aspose.Note kompatibilis a legújabb Java-verziókkal?

2. válasz: Igen, az Aspose.Note kompatibilis a legújabb Java-verziókkal.

### 3. kérdés: Átalakíthatom a OneNote dokumentumokat más formátumokba az Aspose.Note segítségével?

3. válasz: Igen, az Aspose.Note támogatja a OneNote-dokumentumok konvertálását különféle formátumokká, például PDF, DOCX és HTML.

### 4. kérdés: Az Aspose.Note támogatja a OneNote-dokumentumok titkosítását és visszafejtését?

4. válasz: Igen, az Aspose.Note API-kat biztosít a OneNote-dokumentumok titkosításához és visszafejtéséhez.

### 5. kérdés: Az Aspose.Note alkalmas kereskedelmi használatra?

V5: Igen, az Aspose.Note licenc megvásárlásával kereskedelmi célokra használható.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
