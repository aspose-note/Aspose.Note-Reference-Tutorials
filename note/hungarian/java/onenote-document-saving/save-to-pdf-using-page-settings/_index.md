---
title: Mentés PDF-be a OneNote oldalbeállításaival – Aspose.Note
linktitle: Mentés PDF-be a OneNote oldalbeállításaival – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan mentheti a OneNote-dokumentumokat PDF-formátumba Java nyelven az Aspose.Note könyvtár használatával. Lépésről lépésre útmutató kódpéldákkal a különböző oldalbeállításokhoz.
weight: 19
url: /hu/java/onenote-document-saving/save-to-pdf-using-page-settings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mentés PDF-be a OneNote oldalbeállításaival – Aspose.Note

## Bevezetés

Ebből az oktatóanyagból megtudhatja, hogyan mentheti a OneNote-dokumentumokat PDF formátumba különböző oldalbeállítások használatával az Aspose.Note for Java segítségével. Két módszert ismertetünk: a Letter oldalbeállításokkal történő mentést és az A4-es oldalbeállításokkal történő mentést magasságkorlátozás nélkül.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

1. Java Development Kit (JDK) telepítve a rendszerére.
2. Aspose.Note for Java könyvtár letöltve és belekerült a Java projektbe.
3. A Java programozási nyelv alapvető ismerete.

## Csomagok importálása

Győződjön meg arról, hogy importálta az Aspose.Note for Java használatához szükséges csomagokat a projektben. Íme az import nyilatkozat:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Mentés PDF-be a Letter Page Settings segítségével

### 1. lépés: Töltse be a dokumentumot

Először töltse be a OneNote-dokumentumot az Aspose-ba.Megjegyzés:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 2. lépés: Határozza meg a cél útvonalát

Adja meg a PDF-fájl célútvonalát:

```java
String dst = "path/to/your/SaveToPdfUsingLetterPageSettings.pdf";
```

### 3. lépés: Mentse el a dokumentumot

Mentse el a dokumentumot a Letter oldal beállításaival:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getLetter());
oneFile.save(dst, options);
```

## Mentés PDF-be A4-es oldalbeállításokkal magasságkorlátozás nélkül

### 1. lépés: Töltse be a dokumentumot

Hasonlóképpen töltse be a OneNote-dokumentumot az Aspose-ba.Note:

```java
Document oneFile = new Document("path/to/your/OneNote.one");
```

### 2. lépés: Határozza meg a cél útvonalát

Adja meg a PDF-fájl célútvonalát:

```java
String dst = "path/to/your/SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf";
```

### 3. lépés: Mentse el a dokumentumot

A dokumentum mentése A4-es oldalbeállításokkal magasságkorlátozás nélkül:

```java
PdfSaveOptions options = new PdfSaveOptions();
options.setPageSettings(PageSettings.getA4NoHeightLimit());
oneFile.save(dst, options);
```

Az alábbi lépések végrehajtása után sikeresen elmentheti OneNote-dokumentumát PDF formátumba különböző oldalbeállítások használatával.

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan mentheti a OneNote-dokumentumokat PDF formátumba az Aspose.Note for Java könyvtár használatával. A lépésenkénti útmutató követésével könnyedén integrálhatja ezt a funkciót Java-alkalmazásaiba.

## GYIK

### 1. kérdés: Tovább szabhatom az oldalbeállításokat?

1. válasz: Igen, az Aspose.Note for Java segítségével testreszabhatja az oldalbeállításokat igényei szerint.

### 2. kérdés: Az Aspose.Note a PDF-en kívül más kimeneti formátumokat is támogat?

2. válasz: Igen, az Aspose.Note különféle kimeneti formátumokat támogat, beleértve a képeket és a HTML-t.

### 3. kérdés: Az Aspose.Note kompatibilis a OneNote-fájlok különböző verzióival?

3. válasz: Igen, az Aspose.Note támogatja a különböző verziójú OneNote-fájlokat, beleértve a .one-t és az .onetoc2-t.

### 4. kérdés: Konvertálhatok több OneNote-fájlt PDF-be egyetlen futtatással?

4. válasz: Igen, az Aspose.Note for Java használatával több OneNote-fájl kötegelt feldolgozására is lehetőség van.

### 5. kérdés: Elérhető-e próbaverzió tesztelési célokra?

5. válasz: Igen, letöltheti az Aspose.Note for Java ingyenes próbaverzióját a webhelyről.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
