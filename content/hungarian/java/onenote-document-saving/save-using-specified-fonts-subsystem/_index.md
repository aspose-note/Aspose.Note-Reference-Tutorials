---
title: Mentés megadott betűtípus-alrendszer használatával a OneNote-ban
linktitle: Mentés megadott betűtípus-alrendszer használatával a OneNote-ban
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan menthet OneNote-dokumentumokat adott betűtípus-alrendszer használatával Java nyelven az Aspose.Note segítségével. Gondoskodjon a konzisztens betűtípus-megjelenítésről minden platformon, erőfeszítés nélkül.
type: docs
weight: 22
url: /hu/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## Bevezetés

Az Aspose.Note for Java robusztus képességeket biztosít a OneNote-dokumentumokkal való munkavégzéshez. Az ilyen dokumentumokkal való munka során az egyik általános követelmény a betűtípusok megfelelő karbantartása, különösen akkor, ha a dokumentumot különböző formátumokban, például PDF-ben kell exportálni vagy menteni. Ez az oktatóanyag végigvezeti a OneNote-dokumentumok mentésének folyamatán, miközben megadja a betűtípus-alrendszert, biztosítva a szöveg egységes és pontos megjelenítését a különböző platformokon.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy beállította a következő előfeltételeket:

### 1. Java fejlesztőkészlet (JDK)

 Győződjön meg arról, hogy a Java Development Kit (JDK) telepítve van a rendszerén. Letöltheti innen[itt](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) ha még nem tetted meg.

### 2. Aspose.Note for Java Library

 Töltse le és állítsa be az Aspose.Note for Java könyvtárat. Letöltheti a[weboldal](https://releases.aspose.com/note/java/).

## Csomagok importálása

Ügyeljen arra, hogy importálja a szükséges csomagokat a Java projektbe:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Most bontsuk le az egyes példákat több lépésre, hogy jobban megértsük a folyamatot.

## 1. lépés: Mentés a dokumentum-betűtípusok alrendszer használatával az alapértelmezett betűtípusnévvel

Ez a lépés bemutatja, hogyan menthet el egy dokumentumot PDF formátumban egy megadott alapértelmezett betűtípusnév használatával.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document("missing-font.one");

    // Adja meg az alapértelmezett betűtípust.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Mentse el a dokumentumot PDF formátumban.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Ebben a lépésben:
- A OneNote-dokumentum az Aspose.Note használatával töltődik be.
- Az alapértelmezett betűtípus "Times New Roman"-ként van megadva.
- A dokumentum PDF formátumban kerül mentésre a megadott betűtípussal.

## 2. lépés: Mentés a dokumentum-betűtípusok alrendszer használatával az alapértelmezett betűtípussal a fájlból

Ez a lépés bemutatja, hogyan menthet el egy dokumentumot PDF formátumban egy fájlból betöltött alapértelmezett betűtípus használatával.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document("missing-font.one");

    // Adja meg a fontfájl elérési útját.
    String fontFile = "geo_1.ttf";

    // Adja meg az alapértelmezett betűtípust a fájlból.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Mentse el a dokumentumot PDF formátumban.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Ebben a lépésben:
- A "geo_1.ttf" betűtípusfájl betöltődik.
- Az alapértelmezett betűtípust a betöltött betűtípusfájl adja meg.
- A dokumentum PDF formátumban kerül mentésre a megadott betűtípussal.

## 3. lépés: Mentés a dokumentum-betűtípusok alrendszer használatával az adatfolyam alapértelmezett betűtípusával

Ez a lépés bemutatja, hogyan menthet el egy dokumentumot PDF formátumban egy adatfolyamból betöltött alapértelmezett betűtípus használatával.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document("missing-font.one");

    // Adja meg a fontfájl elérési útját.
    String fontFile = "geo_1.ttf";

    // Töltse be a fontfájlt adatfolyamként.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Adja meg az adatfolyam alapértelmezett betűtípusát.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Mentse el a dokumentumot PDF formátumban.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Ebben a lépésben:
- A "geo_1.ttf" betűtípusfájl adatfolyamként betöltődik.
- Az alapértelmezett betűtípust a betöltött adatfolyam határozza meg.
- A dokumentum PDF formátumban kerül mentésre a megadott betűtípussal.

## Következtetés

Ebben az oktatóanyagban megtanultuk, hogyan lehet OneNote-dokumentumokat menteni adott betűtípus-alrendszer használatával Java nyelven az Aspose.Note segítségével. Ha követi ezeket a lépéseket, a dokumentumok exportálásakor vagy mentésekor egységes betűtípus-ábrázolást biztosíthat a különböző platformokon.

## GYIK

### 1. kérdés: Megadhatok különböző betűtípusokat a dokumentum különböző részeihez?

1. válasz: Igen, az Aspose.Note for Java segítségével különböző betűtípusokat adhat meg a dokumentum különböző részeihez.

### 2. kérdés: Az Aspose.Note kompatibilis a OneNote összes verziójával?

2. válasz: Az Aspose.Note a OneNote különféle verzióit támogatja, biztosítva a kompatibilitást a különböző környezetekben.

### 3. kérdés: Hogyan kezelhetem a hiányzó betűtípusokat dokumentumok mentésekor?

3. válasz: Az Aspose.Note lehetőséget biztosít az alapértelmezett betűtípusok megadására a hiányzó betűtípusok hatékony kezeléséhez a dokumentummentés során.

### 4. kérdés: Testreszabhatom a betűtípus tulajdonságait, például a méretet és a stílust?

4. válasz: Igen, személyre szabhatja a betűtípus tulajdonságait, például a méretet, stílust és színt az Aspose.Note for Java segítségével.

### 5. kérdés: Elérhető az Aspose.Note for Java próbaverziója?

5. válasz: Igen, letöltheti az Aspose.Note for Java ingyenes próbaverzióját a webhelyről.