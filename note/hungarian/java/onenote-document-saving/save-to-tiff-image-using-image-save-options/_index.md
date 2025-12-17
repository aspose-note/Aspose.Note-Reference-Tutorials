---
date: 2025-12-17
description: Tudja meg, hogyan menthet OneNote dokumentumokat TIFF fájlokként TIFF
  JPEG tömörítéssel, PackBits-szal vagy CCITT Group 3 Fax-szal Java-ban. Az Aspose.Note
  segítségével szabályozhatja a képminőséget, a fájlméretet és a színmódot.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Mentés TIFF képre TIFF JPEG tömörítéssel a OneNote-ban
url: /hu/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# TIFF kép mentése TIFF JPEG tömörítéssel a OneNote-ban

## Bevezetés

Ebben az útmutatóban megtudja, **hogyan menthet egy OneNote dokumentumot TIFF fájlba TIFF JPEG tömörítéssel**, valamint két másik népszerű tömörítési módszerrel. Végigvezetjük a szükséges beállításokon, importáljuk a szükséges Java csomagokat, és világos lépésről‑lépésre kódot biztosítunk minden tömörítési lehetőséghez. A végére képes lesz **a TIFF képminőség** szabályozására, a fájlméret csökkentésére, sőt fekete‑fehér TIFF-eket is előállítani fax‑stílusú kimenethez.

## Gyors válaszok
- **Mi az a TIFF JPEG tömörítés?** Egy veszteséges tömörítési módszer, amely csökkenti a TIFF fájlméretet miközben megőrzi a vizuális minőséget.  
- **Melyik könyvtár kezeli a konverziót?** Aspose.Note for Java.  
- **Szükségem van licencre?** Egy ingyenes próba működik teszteléshez; licenc szükséges a termeléshez.  
- **Módosíthatom a képminőséget?** Igen, állítsa be a `quality` tulajdonságot az `ImageSaveOptions`-on.  
- **Lehetséges a kötegelt konverzió?** Teljesen – iteráljon a dokumentumokon és alkalmazza ugyanazokat a beállításokat.

## Mi az a TIFF JPEG tömörítés?

A TIFF JPEG tömörítés a képadatokat a TIFF konténerben tárolja, de a JPEG veszteséges algoritmusát alkalmazza a fájl zsugorításához. Ideális, ha egyensúlyt kell találnia a **tiff képminőség** és a kisebb fájlméret között, különösen webes vagy archiválási helyzetekben.

## Miért használjunk különböző TIFF tömörítési típusokat?
- **JPEG** – Jó fényképekhez; állítható minőséget kínál.  
- **PackBits** – Egyszerű, veszteségmentes futamhosszú kódolás; hasznos grafikai elemekhez nagy egységes területekkel.  
- **CCITT Group 3 Fax** – Csak fekete‑fehér; tökéletes beolvasott dokumentumokhoz és fax átvitelhez.  

A megfelelő tömörítés kiválasztása lehetővé teszi, hogy megfeleljen a tárolási korlátoknak anélkül, hogy feláldozná az alkalmazásához szükséges vizuális hűséget.

## Előfeltételek

- Java Development Kit (JDK) telepítve.  
- Aspose.Note for Java könyvtár hozzáadva a projekthez (Maven/Gradle vagy manuális JAR).  
- Alapvető ismeretek a Java szintaxisról.

## Csomagok importálása

Először hozza be a szükséges Aspose.Note osztályokat a Java fájlba:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 1. lépés: TIFF mentése TIFF JPEG tömörítéssel

Az alábbiakban a teljes metódus látható, amely betölti a OneNote fájlt és TIFF‑ként JPEG tömörítéssel menti. Állítsa be a `quality` értéket (0‑100) a **tiff képminőség** szabályozásához.

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Magyarázat**

- `ImageSaveOptions` megmondja az Aspose.Note-nak, hogy TIFF fájlt állítson elő.  
- `setTiffCompression(TiffCompression.Jpeg)` JPEG tömörítést választ.  
- `setQuality(93)` (opcionális) finomhangolja a képminőséget; alacsonyabb értékek kisebb fájlokat eredményeznek.

### Hogyan mentse a TIFF-et JPEG tömörítéssel Java-ban
1. Mutassa a `dataDir`-t arra a mappára, amely a `.one` fájlt tartalmazza.  
2. Hívja meg a `SaveToTiffUsingJpegCompression()`-t a fő metódusból vagy szolgáltatásból.  
3. A keletkezett `.tiff` fájl ugyanabban a könyvtárban jelenik meg.

## 2. lépés: TIFF mentése PackBits tömörítéssel

Ha veszteségmentes opcióra van szüksége, a PackBits egy egyszerű futamhosszú algoritmus, amely jól működik szilárd színekkel rendelkező grafikákhoz.

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Magyarázat**

- `setTiffCompression(TiffCompression.PackBits)` átváltja a tömörítési módszert.  
- Minőségi beállítás nem szükséges, mivel a PackBits veszteségmentes.

## 3. lépés: TIFF mentése CCITT Group 3 Fax tömörítéssel (fekete‑fehér TIFF)

Fax‑stílusú dokumentumokhoz gyakran egy **fekete‑fehér TIFF**-re van szükség. A CCITT Group 3 magas tömörítést biztosít a monokróm képekhez.

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Magyarázat**

- `setColorMode(ColorMode.BlackAndWhite)` monokróm kimenetet kényszerít.  
- `setTiffCompression(TiffCompression.Ccitt3)` a fax‑orientált tömörítést alkalmazza.

## Általános problémák és tippek

| Probléma | Megoldás |
|----------|----------|
| **A kimeneti fájl nagyobb, mint várható** | Próbálja csökkenteni a JPEG `quality` értékét, vagy váltson PackBits-re, ha a veszteségmentes elfogadható. |
| **A színek kifakultak** | Győződjön meg róla, hogy nem állította be véletlenül a `ColorMode.BlackAndWhite`-t, amikor teljes színre van szükség. |
| **Nem támogatott képfájl formátum hiba** | Ellenőrizze, hogy a legújabb Aspose.Note verziót használja; a régebbi build-ek hiányozhatnak bizonyos tömörítési enumok. |
| **LicenseException futásidőben** | Telepítsen érvényes Aspose.Note licencet (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Gyakran feltett kérdések

**K: Átalakíthatok más dokumentumtípusokat (pl. PDF, DOCX) TIFF-re ezekkel a beállításokkal?**  
**V:** Igen. Az Aspose.Note a OneNote fájlokra fókuszál, de az Aspose többi könyvtára (PDF, Words) hasonló `ImageSaveOptions`-t biztosít a saját formátumaikhoz.

**K: Miben különbözik a TIFF JPEG tömörítés a szabványos JPEG fájloktól?**  
**V:** A képadatokat egy TIFF konténerben tárolják, megőrizve a metaadatokat és több oldalt is lehetővé téve, míg a tömörítési algoritmus továbbra is JPEG.

**K: Lehetséges kötegelt feldolgozni sok `.one` fájlt?**  
**V:** Teljesen. Iteráljon egy mappán, hívja meg a három módszer bármelyikét fájlonként, és gyűjtse össze a keletkezett TIFF-eket.

**K: Szabályozhatom a kimeneti TIFF DPI/jelölését?**  
**V:** Igen. Használja a `options.setResolution(int dpi)`-t a mentés előtt.

**K: Támogatja az Aspose.Note az aszinkron feldolgozást?**  
**V:** Az API önmagában szinkron, de a hívásokat Java `CompletableFuture`-be vagy szálkészletekbe csomagolva párhuzamosan futtathatja.

## Összegzés

Most már rendelkezik egy teljes, **java tiff konverzió** eszközkészlettel, amely lehetővé teszi a OneNote dokumentumok TIFF fájlokként való mentését JPEG, PackBits vagy CCITT Group 3 Fax tömörítéssel. Állítsa be a minőséget, a színmódot és a felbontást a saját **tiff képminőség** igényeihez, és integrálja ezeket a módszereket kötegelt munkafolyamatokba a maximális hatékonyság érdekében.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}