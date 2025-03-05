---
title: Mentés TIFF-képbe a OneNote képmentési beállításaival
linktitle: Mentés TIFF-képbe a OneNote képmentési beállításaival
second_title: Aspose.Note Java API
description: Konvertálja a OneNote-dokumentumokat TIFF-re, és szabályozza a fájlméretet és -minőséget! Java nyelven válassza a Jpeg, PackBits vagy Fax tömörítést. Szerezzen kódpéldákat és tanulja meg, hogyan! #OneNote #Java #Aspose
type: docs
weight: 21
url: /hu/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
---
## Bevezetés

Ebből az oktatóanyagból megtudhatja, hogyan menthet dokumentumot TIFF képformátumba az Aspose.Note for Java különböző tömörítési módszereivel. Kitérünk az előfeltételekre, a csomagok importálására, és lépésről lépésre útmutatót adunk minden egyes tömörítési módhoz.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik az alábbiakkal:

- Java Development Kit (JDK) telepítve a rendszerére.
- Aspose.Note for Java könyvtár letöltve és konfigurálva.
- A Java programozási nyelv alapvető ismerete.

## Csomagok importálása

Először importálnia kell a szükséges csomagokat a Java fájlba:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 1. lépés: Mentés TIFF-re JPEG-tömörítéssel

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // A dokumentumok könyvtárának elérési útja.
    String dataDir = "Your Document Directory";

    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

-  Töltse be a dokumentumot a segítségével`Document` osztály.
-  Hozzon létre egy példányt a`ImageSaveOptions` és adja meg a TIFF tömörítési típust JPEG-ként.
- Állítsa be a kívánt minőséget (opcionális).
- Mentse a dokumentumot TIFF formátumba a megadott beállításokkal.

## 2. lépés: Mentse TIFF-re PackBits tömörítéssel

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // A dokumentumok könyvtárának elérési útja.
    String dataDir = "Your Document Directory";

    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

-  Töltse be a dokumentumot a segítségével`Document` osztály.
-  Hozzon létre egy példányt a`ImageSaveOptions` és adja meg a TIFF tömörítési típust PackBits-ként.
- Mentse a dokumentumot TIFF formátumba a megadott beállításokkal.

## 3. lépés: Mentés TIFF-re a CCITT Group 3 faxtömörítés használatával

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // A dokumentumok könyvtárának elérési útja.
    String dataDir = "Your Document Directory";

    // Töltse be a dokumentumot az Aspose.Note-ba.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

-  Töltse be a dokumentumot a segítségével`Document` osztály.
-  Hozzon létre egy példányt a`ImageSaveOptions` és adja meg a TIFF tömörítési típust CCITT Group 3 Faxként.
- Állítsa a színmódot fekete-fehérre.
- Mentse a dokumentumot TIFF formátumba a megadott beállításokkal.

## Következtetés

Ebben az oktatóanyagban megtanulta, hogyan menthet dokumentumot TIFF képformátumba az Aspose.Note for Java különböző tömörítési módszereivel. A lépésenkénti útmutató követésével hatékonyan használhatja ki az Aspose.Note képességeit, hogy megfeleljen igényeinek.

## GYIK

### 1. kérdés: Az Aspose.Note for Java segítségével konvertálhatok más dokumentumformátumokat TIFF formátumba?

1. válasz: Igen, az Aspose.Note for Java támogatja a különféle dokumentumformátumok konvertálását TIFF-re, beleértve a OneNote dokumentumokat is.

### 2. kérdés: Mi a jelentősége a tömörítési típus megadásának TIFF-re történő mentéskor?

2. válasz: A tömörítési típus megadásával szabályozhatja a képminőséget és a fájlméretet. A különböző tömörítési módszerek kompromisszumot kínálnak a minőség és a tömörítési arány között.

### 3. kérdés: Az Aspose.Note for Java alkalmas dokumentumok kötegelt feldolgozására?

3. válasz: Igen, az Aspose.Note for Java API-kat biztosít a kötegelt feldolgozáshoz, lehetővé téve a dokumentumkonverziós feladatok hatékony automatizálását.

### 4. kérdés: Testreszabhatom a tömörítési beállításokat?

V4: Igen, beállíthatja az olyan paramétereket, mint a minőség, a felbontás és a tömörítési módszer, hogy a kimenetet az Ön igényei szerint szabja.

### 5. kérdés: Az Aspose.Note for Java technikai támogatást nyújt?

5. válasz: Igen, az Aspose átfogó technikai támogatást nyújt fórumokon és jegyalapú rendszereken keresztül.