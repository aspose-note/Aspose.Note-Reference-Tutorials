---
date: 2026-03-24
description: Ismerje meg, hogyan menthet OneNote-ot PNG formátumban beállításokkal
  az Aspose.Note for Java segítségével. Ez az útmutató bemutatja, hogyan exportálhatja
  a OneNote-ot képként, hogyan állíthatja be a kép felbontását Java-ban, és hogyan
  konvertálhatja a OneNote-ot programozottan képpé.
linktitle: Convert Notebook to Image with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: OneNote mentése PNG formátumban beállításokkal – Jegyzetfüzet konvertálása
  képpé az Aspose.Note segítségével
url: /hu/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote mentése PNG-ként beállításokkal – Jegyzetfüzet konvertálása képpé

## Bevezetés

Ebben az oktatóanyagban megtudja, hogyan **mentse a OneNote-ot PNG formátumban** a képparaméterek teljes szabályozásával az Aspose.Note for Java segítségével. Akár jelentéskészítéshez, bélyegkép-generáláshoz vagy archiváláshoz kell a OneNote-ot képként exportálni, az alábbi lépések végigvezetik a OneNote jegyzetfüzet képpé konvertálásán, miközben **kép felbontását Java‑stílusban** állítja be a kristálytiszta eredményért.

## Gyors válaszok
- **Választhatok képméretet?** Igen – a `SaveFormat` módosításával exportálhat PNG, JPEG, BMP stb. formátumokba.
- **Hogyan szabályozhatom a kép minőségét?** Használja az `ImageSaveOptions.setResolution()` metódust a DPI (pl. 400 dpi) megadásához.
- **Szükség van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges a nem‑próba használathoz.
- **Az API kompatibilis a Java 8+ verzióval?** Teljesen, az Aspose.Note támogatja a Java 8‑at és újabb verziókat.
- **Több jegyzetfüzetet tudok egyszerre feldolgozni?** Igen – ciklusba foglalva a jegyzetfüzeteket, ugyanazokat a mentési beállításokat alkalmazhatja.

## Mi az a „save onenote as png”?
A OneNote PNG‑ként való mentése azt jelenti, hogy a teljes jegyzetfüzetet (vagy egyes szekciókat) raszteres képekké alakítja. A PNG veszteségmentes, így ideális a jegyzetek, rajzok és beágyazott média vizuális hűségének megőrzésére.

## Miért exportáljuk a OneNote-ot képként beállításokkal?
A OneNote képként való exportálása lehetővé teszi a tartalom megosztását olyan felhasználókkal, akiknek nincs OneNote telepítve, a jegyzetek beágyazását weboldalakba, vagy nagy felbontású PDF‑ek generálását. Az Aspose.Note segítségével **konvertálhatja a OneNote-ot képpé**, miközben testre szabja a felbontást, színmélységet és a kimeneti formátumot – mindezt Java kódból.

## Előfeltételek

1. Java Development Kit (JDK) telepítve a gépén.  
2. Aspose.Note for Java JAR fájlok. Töltse le a könyvtárat [itt](https://releases.aspose.com/note/java/) és adja hozzá a projekt osztályútvonalához.

## Csomagok importálása

Először importálja a szükséges osztályokat:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Lépésről‑lépésre útmutató

### 1. lépés: A jegyzetfüzet betöltése
Töltse be azt a OneNote jegyzetfüzetet, amelyet konvertálni szeretne.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

### 2. lépés: Mentési beállítások megadása
Hozzon létre egy `NotebookImageSaveOptions` példányt, válassza a PNG formátumot, és **állítsa be a kép felbontását Java‑stílusban**.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

### 3. lépés: A jegyzetfüzet mentése képként
Adja meg a kimeneti útvonalat, majd hívja meg a `save` metódust. Ez **PNG‑ként menti a OneNote-ot** a megadott felbontással.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Gyakori problémák és tippek

- **A felbontás nem érvényesül:** Győződjön meg róla, hogy a `getDocumentSaveOptions()` hívást a felbontás beállítása előtt végzi; ellenkező esetben az alap DPI kerül használatra.  
- **Fájl nem található:** Ellenőrizze, hogy a `dataDir` a megfelelő mappára mutat, és hogy a `test.onetoc2` létezik.  
- **Nagy jegyzetfüzetek:** Nagyon nagy jegyzetfüzetek esetén növelje a JVM heap méretét (`-Xmx`), hogy elkerülje a `OutOfMemoryError` hibát.

## Összegzés

Most már tudja, hogyan **mentse a OneNote-ot PNG‑ként** egyedi beállításokkal, hatékonyan **exportálja a OneNote-ot képként** és **konvertálja a OneNote-ot képpé**, miközben szabályozza a felbontást. Integrálja ezeket a kódrészleteket Java alkalmazásaiba a jegyzetfüzetek automatizált feldolgozásához, bélyegképek generálásához vagy archivált másolatok tökéletes vizuális minőséggel történő létrehozásához.

## GyIK

### Q1: Kezelni tudja az Aspose.Note a komplex OneNote fájlokat?
A1: Igen, az Aspose.Note hatékonyan kezeli a komplex OneNote fájlokat, lehetővé téve különféle műveletek programozott végrehajtását.

### Q2: Az Aspose.Note for Java könnyen integrálható meglévő projektekbe?
A2: Teljes mértékben! Az Aspose.Note for Java egyszerű API‑t kínál, amely könnyen beilleszthető Java projektekbe, időt és erőfeszítést takarítva meg.

### Q3: Testreszabhatom a kép kimenetet a jegyzetfüzet konvertálásakor?
A3: Igen, az Aspose.Note lehetővé teszi a kép kimenet testreszabását, például felbontás, formátum és egyéb beállítások megadásával.

### Q4: Nyújt az Aspose.Note fejlesztői támogatást?
A4: Igen, az Aspose kiváló támogatást biztosít fejlesztőknek fórumokon és dokumentációban, elősegítve a zökkenőmentes integrációt és a hibakeresést.

### Q5: Van ingyenes próba a Aspose.Note for Java-hoz?
A5: Igen, ingyenes próbaverziót igényelhet a Aspose.Note for Java‑ból [itt](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utolsó frissítés:** 2026-03-24  
**Tesztelt verzió:** Aspose.Note for Java (legújabb)  
**Szerző:** Aspose  

---