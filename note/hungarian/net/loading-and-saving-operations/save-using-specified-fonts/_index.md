---
title: Mentés megadott betűtípusokkal az Aspose.Note-ban
linktitle: Mentés megadott betűtípusokkal az Aspose.Note-ban
second_title: Aspose.Note .NET API
description: Ismerje meg, hogyan menthet dokumentumokat meghatározott betűtípusokkal az Aspose.Note for .NET webhelyen. Egyszerűen testreszabhatja a betűtípus-beállításokat a konzisztens dokumentumformázás érdekében.
weight: 28
url: /hu/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mentés megadott betűtípusokkal az Aspose.Note-ban

## Bevezetés

Ebből az oktatóanyagból megtudjuk, hogyan mentheti el a dokumentumokat meghatározott betűtípusok használatával az Aspose.Note for .NET-ben. Különféle módszereket fogunk megvizsgálni ennek eléréséhez, lépésről lépésre.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

1.  Aspose.Note for .NET: Győződjön meg arról, hogy telepítette az Aspose.Note for .NET-et. Letöltheti innen[itt](https://releases.aspose.com/note/net/).

2. Fejlesztői környezet: A .NET fejlesztéshez beállított fejlesztői környezetre van szüksége.

## Névterek importálása

Először is importáljuk a szükséges névtereket:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## 1. lépés: Mentés az alapértelmezett betűtípusnévvel

Ebben a lépésben elmentünk egy dokumentumot egy megadott alapértelmezett betűtípusnévvel.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // A dokumentumok könyvtárának elérési útja.
    string dataDir = "Your Document Directory";

    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Mentse el a dokumentumot PDF-ként megadott alapértelmezett betűtípussal.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## 2. lépés: Mentés alapértelmezett betűtípussal a fájlból

Ezután mentsünk el egy dokumentumot egy fájlból betöltött alapértelmezett betűtípus használatával.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // A dokumentumok könyvtárának elérési útja.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Mentse el a dokumentumot PDF formátumban a fájlból betöltött alapértelmezett betűtípussal.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## 3. lépés: Mentés alapértelmezett betűtípussal a Streamből

Végül mentsünk el egy dokumentumot egy adatfolyamból betöltött alapértelmezett betűtípus használatával.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // A dokumentumok könyvtárának elérési útja.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Mentse a dokumentumot PDF formátumban az adatfolyamból betöltött alapértelmezett betűtípussal.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan menthetünk el dokumentumokat meghatározott betűtípusok használatával az Aspose.Note for .NET-ben. Ha követi ezeket a lépéseket, testreszabhatja a betűtípus-beállításokat az igényeinek megfelelően, így biztosítva, hogy a dokumentumok a kívánt formázást kapják.

## GYIK

### 1. kérdés: Használhatok bármilyen betűtípust dokumentumok mentésére az Aspose.Note-ban?

V1: Igen, bármilyen betűtípust megadhat a dokumentumok mentéséhez. Csak győződjön meg arról, hogy a fontfájl elérhető és megfelelően betöltődik.

### 2. kérdés: Az Aspose.Note kompatibilis a különböző dokumentumformátumokkal?

2. válasz: Az Aspose.Note elsősorban a OneNote-dokumentumokkal működik, de lehetőséget biztosít különféle formátumokban történő mentésre, beleértve a PDF-formátumot is.

### 3. kérdés: Hogyan kezelhetem a hiányzó betűtípusokat dokumentumok mentésekor?

3. válasz: Az Aspose.Note lehetőséget kínál az alapértelmezett betűtípusok használatára arra az esetre, ha a megadott betűtípus hiányzik, így biztosítva a konzisztens dokumentumformázást.

### 4. kérdés: Az Aspose.Note támogatja a betűtípusok beágyazását a kimeneti dokumentumokba?

4. válasz: Igen, az Aspose.Note lehetővé teszi a betűtípusok beágyazását, hogy biztosítsa a dokumentumok hordozhatóságát és a konzisztens megjelenítést a különböző platformokon.

### 5. kérdés: Hol kaphatok további segítséget az Aspose.Note-tal kapcsolatban?

 5. válasz: További segítségért vagy technikai támogatásért keresse fel a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
