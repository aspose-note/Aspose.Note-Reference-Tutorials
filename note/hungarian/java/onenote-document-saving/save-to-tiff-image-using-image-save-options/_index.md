---
date: 2026-03-14
description: Ismerje meg, hogyan menthet OneNote dokumentumokat TIFF fájlokként TIFF
  JPEG tömörítéssel, TIFF PackBits tömörítéssel vagy CCITT Group 3 Fax használatával
  Java-ban. Szabályozza a képminőséget, a fájlméretet és a színmódot az Aspose.Note
  segítségével.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Mentés TIFF képre a OneNote‑ban TIFF JPEG tömörítéssel
url: /hu/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# TIFF kép mentése TIFF JPEG tömörítéssel a OneNote-ban

## Bevezetés

Ebben az útmutatóban megtudja, **hogyan menthet egy OneNote dokumentumot TIFF fájlba TIFF JPEG tömörítéssel**, valamint két másik népszerű tömörítési módszerrel. Végigvezetjük a szükséges beállításokon, importáljuk a szükséges Java csomagokat, és világos lépésről‑lépésre kódot biztosítunk minden tömörítési opcióhoz. A végére képes lesz **a TIFF képminőség** szabályozására, a fájlméret csökkentésére, és akár fekete‑fehér TIFF-eket is előállítani fax‑stílusú kimenethez.

## Gyors válaszok
- **Mi az a TIFF JPEG tömörítés?** Egy veszteséges tömörítési módszer, amely csökkenti a TIFF fájl méretét, miközben megőrzi a vizuális minőséget.  
- **Melyik könyvtár kezeli a konverziót?** Aspose.Note for Java.  
- **Szükségem van licencre?** Egy ingyenes próba működik teszteléshez; licenc szükséges a termeléshez.  
- **Módosíthatom a képminőséget?** Igen, állítsa be a `quality` tulajdonságot az `ImageSaveOptions`-on.  
- **Lehetséges a kötegelt konverzió?** Természetesen – iteráljon a dokumentumokon, és alkalmazza ugyanazokat a beállításokat.

## Mi az a TIFF JPEG tömörítés?

A TIFF JPEG tömörítés a képadatokat egy TIFF konténerben tárolja, de a JPEG veszteséges algoritmusát alkalmazza a fájl méretének csökkentésére. Ideális, ha egyensúlyt kell megtalálni a **tiff képminőség** és a kisebb fájlméret között, különösen webes vagy archiválási helyzetekben.

## Miért használjunk különböző TIFF tömörítési típusokat?
- **JPEG** – Jó fényképekhez; állítható minőséget kínál.  
- **PackBits** – Egyszerű, veszteségmentes futamhosszú kódolás; hasznos grafikai elemekhez nagy egységes területekkel.  
- **CCITT Group 3 Fax** – Csak fekete‑fehér; tökéletes beolvasott dokumentumokhoz és faxátvitelhez.  

A megfelelő tömörítés kiválasztása lehetővé teszi, hogy megfeleljen a tárolási korlátoknak anélkül, hogy feláldozná az alkalmazásához szükséges vizuális hűséget.

## OneNote konvertálása TIFF-re az Aspose.Note segítségével

Ha a célja **a OneNote TIFF-re konvertálása**, az alábbi három módszer lefedi a leggyakoribb forgatókönyveket. Minden módszer betölt egy `.one` fájlt, konfigurálja az `ImageSaveOptions`-t, és a végeredményt `.tiff` fájlként menti.

## Előkövetelmények

- Telepített Java Development Kit (JDK).  
- Az Aspose.Note for Java könyvtár hozzáadva a projekthez (Maven/Gradle vagy manuális JAR).  
- Alapvető ismeretek a Java szintaxisról.

## Csomagok importálása

Először hozza be a szükséges Aspose.Note osztályokat a Java fájlba:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## 1. lépés: TIFF mentése TIFF JPEG tömörítéssel

Az alábbiakban a teljes metódus látható, amely betölt egy OneNote fájlt, és JPEG tömörítéssel TIFF-ként menti. Állítsa be a `quality` értéket (0‑100) a **tiff képminőség** szabályozásához.

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

- `ImageSaveOptions` azt mondja az Aspose.Note-nak, hogy TIFF fájlt állítson elő.  
- `setTiffCompression(TiffCompression.Jpeg)` JPEG tömörítést választ.  
- `setQuality(93)` (opcionális) finomhangolja a képminőséget; alacsonyabb értékek kisebb fájlokat eredményeznek.

### Hogyan mentse a TIFF-et JPEG tömörítéssel Java-ban
1. Állítsa a `dataDir`-t arra a mappára, amely a `.one` fájlt tartalmazza.  
2. Hívja meg a `SaveToTiffUsingJpegCompression()`-t a fő metódusából vagy szolgáltatásából.  
3. A keletkezett `.tiff` fájl ugyanabban a könyvtárban jelenik meg.

## TIFF PackBits tömörítés áttekintése

A PackBits egy veszteségmentes tömörítési algoritmus, amely a legjobban nagy, egyszínű területekkel rendelkező képeknél működik. A dokumentációban gyakran **tiff packbits compression**-ként hivatkoznak rá.

## 2. lépés: TIFF mentése PackBits tömörítéssel

Ha veszteségmentes opcióra van szüksége, a PackBits egy egyszerű futamhosszú algoritmus, amely jól működik szilárd színekkel rendelkező grafikák esetén.

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
- Nem szükséges minőség beállítása, mivel a PackBits veszteségmentes.

## 3. lépés: TIFF mentése CCITT Group 3 Fax tömörítéssel (fekete‑fehér TIFF)

Fax‑stílusú dokumentumokhoz gyakran egy **fekete‑fehér TIFF**-re van szükség. A CCITT Group 3 magas tömörítést biztosít monokróm képekhez.

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

## Gyakori problémák és tippek

| Probléma | Megoldás |
|----------|----------|
| **A kimeneti fájl nagyobb, mint várható** | Próbálja csökkenteni a JPEG `quality` értékét, vagy váltson PackBits-re, ha a veszteségmentes megoldás elfogadható. |
| **A színek kifakultak** | Győződjön meg róla, hogy nem állította be véletlenül a `ColorMode.BlackAndWhite`-t, amikor teljes színre van szükség. |
| **Nem támogatott képadatforma hiba** | Ellenőrizze, hogy a legújabb Aspose.Note verziót használja; a régebbi build-ek hiányozhatnak bizonyos tömörítési enumok. |
| **LicenseException futásidőben** | Telepítsen érvényes Aspose.Note licencet (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Gyakran Ismételt Kérdések

**Q: Átalakíthatok más dokumentumtípusokat (pl. PDF, DOCX) TIFF-re ezekkel a beállításokkal?**  
A: Igen. Bár az Aspose.Note a OneNote fájlokra fókuszál, az Aspose.PDF, Aspose.Words és más könyvtárak hasonló `ImageSaveOptions`-t biztosítanak a saját formátumaikhoz.

**Q: Miben különbözik a TIFF JPEG tömörítés egy szabványos JPEG fájltól?**  
A: A JPEG algoritmus ugyanaz, de a képadatok egy TIFF konténerben élnek, amely több oldalt és gazdagabb metaadatokat is tárolhat.

**Q: Lehetséges kötegelt feldolgozni sok `.one` fájlt?**  
A: Teljesen. Iteráljon egy könyvtáron, hívja meg a három módszer bármelyikét minden fájlra, és gyűjtse össze a keletkezett TIFF-eket.

**Q: Szabályozhatom a kimeneti TIFF DPI/jelölését?**  
A: Igen. Használja a `options.setResolution(int dpi)`-t mentés előtt.

**Q: Támogatja az Aspose.Note az aszinkron feldolgozást?**  
A: Az API maga szinkron, de a hívásokat be lehet csomagolni a Java `CompletableFuture`-be vagy egy szálkezelőbe a párhuzamos végrehajtáshoz.

## Összegzés

Most már rendelkezik egy teljes **java tiff konverzió** eszközkészlettel, amely lehetővé teszi a OneNote dokumentumok TIFF fájlként való mentését JPEG, PackBits vagy CCITT Group 3 Fax tömörítéssel. Állítsa be a minőséget, a színmódot és a felbontást a saját **tiff képminőség** igényeinek megfelelően, és integrálja ezeket a módszereket kötegelt munkafolyamatokba a maximális hatékonyság érdekében.

---

**Last Updated:** 2026-03-14  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}