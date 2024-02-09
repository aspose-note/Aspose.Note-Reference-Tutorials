---
title: Hozzon létre OneNote-dokumentumot, és mentse HTML-be az Aspose.Note-ban
linktitle: Hozzon létre OneNote-dokumentumot, és mentse HTML-be az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan hozhat létre és menthet Microsoft OneNote dokumentumokat HTML formátumba .NET-alkalmazásokban az Aspose.Note API használatával. Kövesse átfogó oktatóanyagunkat lépésről lépésre példákkal.
type: docs
weight: 14
url: /hu/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Bevezetés

Az Aspose.Note for .NET egy hatékony API, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft OneNote dokumentumokkal .NET-alkalmazásaikban. Az Aspose.Note segítségével könnyedén hozhat létre, kezelhet és konvertálhat OneNote-fájlokat. Ebben az oktatóanyagban megvizsgáljuk, hogyan hozhat létre OneNote-dokumentumot, és hogyan mentheti el HTML formátumba az Aspose.Note for .NET API által biztosított különféle lehetőségek segítségével.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

- C# programozási nyelv alapismerete.
- A Visual Studio telepítve van a rendszerére.
-  Aspose.Note a projektben telepített .NET API-hoz. Letöltheti innen[itt](https://releases.aspose.com/note/net/).
- A Microsoft OneNote dokumentumok szerkezetének ismerete.

## Névterek importálása

Mielőtt belemerülnénk a kódolási részbe, importáljuk a szükséges névtereket:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Most bontsuk le az egyes példákat több lépésre, és nézzük meg, hogyan hozhat létre OneNote-dokumentumot és mentheti el HTML formátumba az Aspose.Note for .NET használatával.

## 1. lépés: Hozzon létre egy OneNote-dokumentumot az alapértelmezett beállításokkal

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Inicializálja a OneNote-dokumentumot
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Alapértelmezett stílus a dokumentumban lévő összes szöveghez.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Mentés HTML formátumba
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

Ebben a lépésben inicializálunk egy új OneNote-dokumentumot, hozzáadunk egy oldalt címmel, és az alapértelmezett beállításokkal HTML formátumba mentjük.

## 2. lépés: Adott oldaltartomány létrehozása és mentése HTML-be

```csharp
public static void CreateAndSavePageRange()
{
    // Inicializálja a OneNote-dokumentumot
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Alapértelmezett stílus a dokumentumban lévő összes szöveghez.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Mentés HTML formátumba
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Itt bemutatjuk, hogyan lehet dokumentumot létrehozni és egy adott oldaltartományt HTML formátumba menteni.

## 3. lépés: Mentse HTML-ként a memóriafolyamba beágyazott erőforrásokkal

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Töltse be a OneNote dokumentumot
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Adja meg a HTML mentési beállításokat
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Mentse el a dokumentumot egy memóriafolyamba
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Ez a lépés bemutatja, hogyan menthet OneNote-dokumentumot HTML formátumba beágyazott erőforrásokkal (CSS, betűtípusok és képek) memóriafolyamba.

## 4. lépés: Mentse el HTML-ként a Fájlba külön fájlokban lévő erőforrásokkal

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Töltse be a OneNote dokumentumot
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Adja meg a HTML mentési beállításokat
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Mentse a dokumentumot HTML-fájlba, külön fájlokban tárolt erőforrásokkal
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

Ebben a lépésben egy OneNote-dokumentumot mentünk HTML formátumba, és minden erőforrást (CSS, betűtípusok és képek) külön fájlokban tárolunk.

## 5. lépés: Mentse HTML-ként a memóriafolyamba visszahívásokkal az erőforrások mentéséhez

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Adja meg a visszahívások mentési konfigurációját
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Adja meg a HTML mentési beállításokat
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Töltse be a OneNote dokumentumot
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Mentse a dokumentumot HTML formátumba a felhasználó által meghatározott visszahívások által kezelt erőforrásokkal
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Adatok manuális hozzáfűzése a CSS-folyamhoz
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Itt bemutatjuk, hogyan menthet OneNote-dokumentumot HTML formátumba a felhasználó által meghatározott visszahívások által kezelt erőforrásokkal.

## Következtetés

Ebben a cikkben megvizsgáltuk, hogyan dolgozhat a OneNote-dokumentumokkal, és hogyan mentheti azokat HTML-formátumba az Aspose.Note for .NET használatával. A lépésenkénti útmutató követésével könnyedén megteheti

 integrálja ezt a funkciót .NET-alkalmazásaiba, lehetővé téve a OneNote-fájlok hatékony kezelését.

## GYIK

### 1. kérdés: Testreszabhatom a mentett HTML-fájl megjelenését?

1. válasz: Igen, testreszabhatja a megjelenést az átalakítási folyamat során generált CSS-stíluslapok módosításával.

### 2. kérdés: Támogatja az Aspose.Note a HTML-en kívül más formátumokba való konvertálást?

2. válasz: Igen, az Aspose.Note támogatja a konvertálást különféle formátumokká, például PDF-ekké, képekké és Microsoft Word-dokumentumokká.

### 3. kérdés: Az Aspose.Note kompatibilis a .NET Core alkalmazásokkal?

3. válasz: Igen, az Aspose.Note kompatibilis a .NET Framework és a .NET Core alkalmazásokkal is.

### 4. kérdés: Kivonhatok szöveget és képeket a OneNote-dokumentumokból az Aspose.Note segítségével?

4. válasz: Igen, az Aspose.Note API segítségével szöveget és képeket bonthat ki, valamint különféle egyéb manipulációkat hajthat végre.

### 5. kérdés: Elérhető-e próbaverzió az Aspose.Note funkcióinak teszteléséhez?

 5. válasz: Igen, letölthet egy ingyenes próbaverziót a webhelyről[itt](https://releases.aspose.com/).