---
date: 2026-09-04
description: Ismerje meg, hogyan exportálhat OneNote oldalt PNG képre Java-ban az
  Aspose.Note használatával. Ez az útmutató bemutatja a .one fájl PNG-re konvertálását,
  az oldal index beállítását és a kép mentését.
keywords:
- how to export onenote
- convert onenote to png
- save onenote as image
- convert .one to png
lastmod: 2026-09-04
linktitle: OneNote oldal exportálása PNG képre Java-ban
og_description: Hogyan exportáljunk OneNote oldalt PNG formátumba Java-ban az Aspose.Note
  segítségével. Ez az útmutató végigvezet a .one fájl betöltésén, egy oldal kiválasztásán
  és egy magas minőségű PNG kép mentésén.
og_image_alt: 'Tutorial: Export OneNote page to PNG image using Aspose.Note for Java'
og_title: Hogyan exportáljunk OneNote oldalt PNG formátumba Java-ban az Aspose.Note
  segítségével
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to export OneNote page to PNG image in Java using Aspose.Note.
    This guide shows converting .one to png, setting the page index, and saving as
    an image.
  headline: How to export OneNote page to PNG in Java with Aspose.Note
  type: TechArticle
- description: Learn how to export OneNote page to PNG image in Java using Aspose.Note.
    This guide shows converting .one to png, setting the page index, and saving as
    an image.
  name: How to export OneNote page to PNG in Java with Aspose.Note
  steps:
  - name: Load the OneNote document
    text: The `Document` class represents a OneNote file in memory. Loading the file
      is the foundation for **convert .one to png**.
  - name: Initialise image‑save options
    text: '`ImageSaveOptions` tells Aspose.Note that the output should be **PNG**.
      You can also adjust DPI, color depth, and compression here.'
  - name: Set the page index (how to convert OneNote page)
    text: The `setPageIndex` method selects which page to export. Page numbering starts
      at **0**, so `0` refers to the first page. Adjust this value to export a different
      page or loop through pages for bulk conversion.
  - name: Save the document as PNG (save OneNote as PNG)
    text: Calling `save` writes the selected page to a PNG file on disk. The file
      name `ConvertSpecificPageToPngImage_out.png` is just an example—you can name
      it whatever you like. This final step **exports onenote page image** ready for
      use in reports, web pages, or further processing.
  type: HowTo
- questions:
  - answer: Aspose.Note for Java.
    question: What library is needed?
  - answer: Yes—use `setPageIndex` to target the exact page.
    question: Can I export a single page?
  - answer: PNG, JPEG, GIF, BMP, TIFF (PNG shown here).
    question: Supported image formats?
  - answer: A free trial is available; a license is required for production.
    question: Do I need a license?
  - answer: Typically under 10 minutes for a basic conversion.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote conversion
- Aspose.Note
- java image export
title: Hogyan exportáljunk OneNote oldalt PNG formátumba Java-ban az Aspose.Note segítségével
url: /hu/java/onenote-document-loading/convert-page-to-png-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan exportáljunk OneNote oldalt PNG formátumba Java-val az Aspose.Note segítségével

Ebben az oktatóanyagban megtanulja, **hogyan exportáljunk OneNote oldalt** PNG képként az Aspose.Note for Java könyvtár használatával. A OneNote oldalak exportálása gyakori igény, amikor a jegyzeteket a OneNote ökoszisztémáján kívül kell megosztani, jelentésekbe beágyazni, vagy képfeldolgozó algoritmusokat futtatni. Kitérünk a környezet beállítására, egy .one fájl betöltésére, egy adott oldal kiválasztására, a képbeállítások konfigurálására, és végül egy nagy felbontású PNG fájl mentésére.

## Gyors válaszok
- **Milyen könyvtárra van szükség?** Aspose.Note for Java.  
- **Exportálhatok egyetlen oldalt?** Igen—használja a `setPageIndex`‑et a pontos oldal kiválasztásához.  
- **Támogatott képfájlformátumok?** PNG, JPEG, GIF, BMP, TIFF (itt PNG látható).  
- **Szükségem van licencre?** Egy ingyenes próba elérhető; licenc szükséges a termeléshez.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 percnél kevesebb egy alap konverzióhoz.  
- **Hogyan konvertáljuk a .one fájlt png‑re?** Töltsük be a `.one` fájlt a `Document`‑dal, állítsuk be az oldal indexet, és mentsük az `ImageSaveOptions`‑szal.  

## Mi az a „export OneNote page”?
A OneNote oldal exportálása azt jelenti, hogy egy adott oldalt a `.one` dokumentumból önálló képfájllá (PNG ebben az esetben) konvertálunk. Ez akkor hasznos, ha **exportálni szeretné a OneNote oldal képét** megosztás, beágyazás vagy további képalapú elemzés céljából. A folyamat a OneNote fájl betöltésével, a kívánt oldal kiválasztásával, majd az oldal raszteres képként való renderelésével kezdődik.

## Miért használjuk az Aspose.Note for Java‑t a OneNote PNG‑re konvertálásához?
Az Aspose.Note **50+ bemeneti és kimeneti formátumot** támogat, és több száz oldalas jegyzetfüzeteket képes renderelni Microsoft Office nélkül. Finomhangolt vezérlést biztosít az oldal kiválasztása, DPI és színmélység felett, így PNG fájlokat hoz létre, amelyek megőrzik a vektoros grafikákat és a szöveg tisztaságát. A könyvtár bármely, Java 8+‑t támogató platformon fut, így ideális szerveroldali kötegelt konverziókhoz.

## Előkövetelmények

1. **Java Development Kit (JDK)** – 8-as vagy újabb verzió.  
2. **Aspose.Note for Java** – töltse le a legújabb JAR‑t az [Aspose website](https://releases.aspose.com/note/java/) oldalról.  
3. **OneNote dokumentum** (`.one`), amely tartalmazza a exportálni kívánt oldalt.

## Csomagok importálása

Először importálja a szükséges Java osztályokat:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.LoadOptions;
import com.aspose.note.SaveFormat;
```

Ezek az importok hozzáférést biztosítanak az Aspose.Note API‑hoz, beleértve a dokumentumok betöltését és a képmentési beállítások konfigurálását.

## Lépésről‑lépésre útmutató

### 1. lépés: OneNote dokumentum betöltése

A `Document` osztály egy OneNote fájlt reprezentál a memóriában. A fájl betöltése a **.one‑ről png‑re konvertálás** alapja.

```java
// Load the document into Aspose.Note.
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", new LoadOptions());
```

### 2. lépés: Képmentési beállítások inicializálása

`ImageSaveOptions` jelzi az Aspose.Note számára, hogy a kimenet **PNG** legyen. Itt állíthatja be a DPI‑t, a színmélységet és a tömörítést is.

```java
// Initialize ImageSaveOptions object
ImageSaveOptions opts = new ImageSaveOptions(SaveFormat.Png);
```

### 3. lépés: Az oldal indexének beállítása (hogyan konvertáljuk a OneNote oldalt)

A `setPageIndex` metódus kiválasztja, melyik oldalt exportálja. Az oldalszámozás **0**‑tól kezdődik, így a `0` az első oldalt jelenti. Állítsa be ezt az értéket egy másik oldal exportálásához vagy a tömeges konverzióhoz ciklusban.

```java
// set page index
opts.setPageIndex(0);
```

### 4. lépés: Dokumentum mentése PNG‑ként (OneNote mentése PNG‑ként)

A `save` hívás a kiválasztott oldalt egy PNG fájlba írja a lemezen. A `ConvertSpecificPageToPngImage_out.png` fájlnév csak példa—bármilyen nevet adhat neki. Ez az utolsó lépés **exportálja a OneNote oldal képét**, amely készen áll a jelentésekben, weboldalakon vagy további feldolgozásban való felhasználásra.

```java
// Save the document as PNG.
oneFile.save(dataDir + "ConvertSpecificPageToPngImage_out.png", opts);
```

## Gyakori problémák és tippek

- **Helytelen oldal index** – Ne feledje, hogy az indexelés 0‑tól kezdődik. Ha üres képet kap, ellenőrizze az index értékét.  
- **Hiányzó Aspose.Note JAR** – Győződjön meg róla, hogy a JAR a classpath‑on van; különben `ClassNotFoundException`-t kap.  
- **Nagy oldalak** – Nagyon nagy oldalak esetén fontolja meg a JVM heap méretének növelését (`-Xmx`), hogy elkerülje a `OutOfMemoryError`-t.  
- **Felbontás szabályozása** – Használja a `opts.setResolution(300)`‑t (vagy a kívánt DPI‑t) a `save` hívása előtt a kép tisztaságának javításához.  

## Gyakran ismételt kérdések

**Q1: Konvertálhatok több oldalt PNG képekké egyszerre az Aspose.Note for Java használatával?**  
A1: Igen, iterálhat a dokumentum oldalain, frissítheti a `opts.setPageIndex(i)`‑t, és minden iterációban meghívhatja a `save`‑t.

**Q2: Az Aspose.Note for Java támogat más képfájlformátumokat is a PNG‑en kívül?**  
A2: Teljesen. Állítsa be a `SaveFormat.Jpeg`, `SaveFormat.Gif`, `SaveFormat.Bmp` vagy `SaveFormat.Tiff` értékeket az `ImageSaveOptions`‑ban a kívánt formátumok generálásához.

**Q3: Van ingyenes próba az Aspose.Note for Java‑hoz?**  
A3: Igen, letölthet egy ingyenes próbaverziót a [Aspose Note download page](https://releases.aspose.com/).

**Q4: Hol kaphatok technikai segítséget, ha problémáim vannak?**  
A5: Kérhet támogatást az Aspose közösségi fórumon [Aspose community forum](https://forum.aspose.com/c/note/28).

**Q5: Hogyan vásárolhatok licencet az Aspose.Note for Java‑hoz?**  
A5: Licencet vásárolhat a [purchase page](https://purchase.aspose.com/buy) oldalon.

**Q6: Hogyan kezelődnek a beágyazott képek exportálás közben?**  
A6: A beágyazott képek automatikusan megjelennek a PNG kimenetben; nincs szükség extra kódra.

**Q7: Beállíthatom a DPI‑t vagy a kép felbontását?**  
A7: Igen, használja a `opts.setResolution(int dpi)`‑t a `save` hívása előtt a kimeneti minőség szabályozásához.

---

**Legutóbb frissítve:** 2026-09-04  
**Tesztelve:** Aspose.Note for Java 24.11 (legújabb)  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [OneNote exportálása BMP képként az Aspose.Note for Java Image Save Options használatával](/note/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/)
- [OneNote oldalak exportálása – Specifikus oldaltartomány konvertálása PDF‑be Java-val](/note/java/onenote-document-loading/convert-page-range-to-pdf/)
- [Tanulja meg a JPEG DPI növelését – Kimeneti kép felbontás beállítása OneNote-ban az Aspose.Note segítségével](/note/java/onenote-document-saving/set-output-image-resolution/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}