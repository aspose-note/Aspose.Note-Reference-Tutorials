---
date: 2025-12-18
description: Ismerje meg, hogyan lehet **OneNote-ot PDF-ként menteni** a Java-ban
  az Aspose.Note megadott betűkészlet alrendszerével. Ez az útmutató bemutatja, hogyan
  lehet OneNote-ot PDF-re konvertálni, egyéni betűkészlet-fájlokat betölteni, és alapértelmezett
  betűkészleteket megadni.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: OneNote mentése PDF-be a megadott betűtípusok alrendszerével
url: /hu/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote mentése PDF-ként a megadott betűkészlet alrendszerrel

## Bevezetés

Sok üzleti helyzetben szükség van arra, hogy **OneNote-ot PDF-ként mentsünk**, miközben megőrzünk az eredeti oldalak pontos megjelenését. Az Aspose.Note for Java ezt egyszerűvé teszi, mivel lehetővé teszi a betűkészlet alrendszerének vezérlését a konvertálás során. Ebben az útmutatóban három gyakorlati módot mutatunk be a **OneNote PDF-re konvertálására**, beleértve a **egyedi betűkészlet fájlok betöltését**, a **alapértelmezett betűkészlet megadását**, és akár a **betűkészlet adatfolyam használatát**, ha a betűkészlet nem érhető el a célgépen.

## Gyors válaszok
- **Mi jelent a “save OneNote as PDF”?** Egy .one fájlt PDF-be konvertál, miközben a elrendezést és a stílusokat érintetlenül hagyja.  
- **Melyik API kezeli a betűkészleteket?** A `DocumentFontsSubsystem` lehetővé teszi alapértelmezett betűkészlet meghatározását vagy egyedi betűkészlet fájl/stream betöltését.  
- **Szükség van licencre a termeléshez?** Igen, kereskedelmi Aspose.Note licenc szükséges a nem‑próbaverzió használatához.  
- **Több fájlt konvertálhatok egyszerre?** Természetesen – csak ciklusba kell tenni a `Document` betöltési és mentési logikáját.  
- **Milyen Java verzió szükséges?** Java 15 vagy újabb (a példa JDK 15-öt használ).

## Mi az a “save OneNote as PDF” betűkészlet alrendszerrel?

A OneNote PDF-be mentése betűkészlet alrendszerrel azt jelenti, hogy a konvertálás során az Aspose.Note minden hiányzó glifet a megadott betűkészlettel helyettesít. Ez garantálja, hogy a PDF minden eszközön azonosuljon, még akkor is, ha az eredeti betűkészlet nincs telepítve.

## Miért kell vezérelni a betűkészlet alrendszert, amikor **OneNote-ot PDF-re konvertálsz**?

- **Következetes márkázás** – a vállalati dokumentumok pontosan ugyanazt a betűtípust tartják.  
- **Keresztplatformos megbízhatóság** – a PDF-ek ugyanúgy jelennek meg Windows, macOS, Linux és mobil rendszereken.  
- **Csökkentett hibák** – a hiányzó betűkészlet figyelmeztetések eltűnnek, tiszta kimenetet eredményezve.

## Előfeltételek

### 1. Java fejlesztői csomag (JDK)

Győződjön meg róla, hogy a rendszerén telepítve van a Java Development Kit (JDK). Letöltheti [innen](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html), ha még nincs.

### 2. Aspose.Note for Java könyvtár

Töltse le és állítsa be az Aspose.Note for Java könyvtárat. Letöltheti a [weboldalról](https://releases.aspose.com/note/java/).

## Csomagok importálása

Győződjön meg róla, hogy importálja a szükséges csomagokat a Java projektjében:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Most bontsuk le minden példát több lépésre, hogy jobban megértsük a folyamatot.

## Hogyan **mentse a OneNote-ot PDF-ként** a Document Fonts Subsystem használatával alapértelmezett betűkészlettel

### 1. lépés: Mentés a Document Fonts Subsystem használatával alapértelmezett betűkészlet névvel

Ez a lépés bemutatja, hogyan **mentse a OneNote-ot PDF-ként** egyszerű módon, egy alapértelmezett betűkészlet nevének megadásával.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

Ebben a lépésben:
- A OneNote dokumentum betöltésre kerül az Aspose.Note segítségével.
- Az **alapértelmezett betűkészlet** **"Times New Roman"** névre van beállítva.
- A dokumentum PDF formátumban mentésre kerül a kiválasztott betűkészlettel.

### 2. lépés: Mentés a Document Fonts Subsystem használatával alapértelmezett betűkészlettel fájlból

Itt **egyedi betűkészlet fájlt töltünk be**, és használjuk visszaesésként a PDF-re konvertáláskor.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

Kulcspontok:
- Az **egyedi betűkészlet fájl** `geo_1.ttf` **lemezről betöltődik**.
- `usingDefaultFontFromFile` **alapértelmezett betűkészletet ad meg fájlból**, biztosítva, hogy a PDF ezt a betűkészletet használja, ha az eredeti hiányzik.
- Az eredményül kapott PDF megőrzi a kívánt megjelenést.

### 3. lépés: Mentés a Document Fonts Subsystem használatával alapértelmezett betűkészlettel adatfolyamból

Néha a betűkészlet adatbázisban vagy hálózaton keresztül érkezhet. Ez a példa bemutatja, hogyan **használjon betűkészlet adatfolyamot**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

Itt történik:
- A betűkészlet fájl **InputStream**‑ként nyílik meg, ami hasznos, ha a betűkészlet nem fájl forrásban van.
- `usingDefaultFontFromStream` **betűkészlet adatfolyamot használ** a visszaeső betűkészlet meghatározásához.
- A OneNote fájl PDF-ként mentésre kerül a stream‑alapú betűkészlettel.

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Hogyan javítsuk |
|----------|------------------|-----------------|
| **Hiányzó betűkészlet figyelmeztetések** | A forrás .one fájl olyan betűkészletet hivatkozik, amely nincs jelen a gépen. | Adj meg alapértelmezett betűkészletet a `usingDefaultFont`, `usingDefaultFontFromFile` vagy `usingDefaultFontFromStream` használatával. |
| **Egyedi betűkészlet fájl nem található** | Helytelen útvonal a `.ttf` fájlhoz. | Használj abszolút útvonalakat vagy ellenőrizd a relatív útvonalat a munkakönyvtárból. |
| **Az adatfolyam nincs lezárva** | Kivétel lép fel a `close()` hívása előtt. | Használj try‑with‑resources‑t (`try (InputStream stream = ...) { ... }`) az automatikus lezáráshoz. |

## Gyakran ismételt kérdések

**K: Megadhatok különböző betűkészleteket a dokumentum különböző részeire?**  
V: Igen, egyedi betűkészlet beállításokat alkalmazhat egyes gazdag szövegelemekre az Aspose.Note `Font` osztályával.

**K: Az Aspose.Note kompatibilis minden OneNote verzióval?**  
V: Az Aspose.Note támogatja a OneNote fájlokat a legújabb asztali és mobil verziókból, biztosítva a széles körű kompatibilitást.

**K: Hogyan kezeljem a hiányzó betűkészleteket a dokumentumok mentésekor?**  
V: Használja a fent bemutatott betűkészlet alrendszer módszereket (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) a visszaesés biztosításához.

**K: Testreszabhatom a betűkészlet tulajdonságait, például méretet és stílust?**  
V: Teljesen – az API lehetővé teszi a méret, stílus, szín és egyéb attribútumok beállítását futásonként.

**K: Elérhető próba verzió az Aspose.Note for Java-hoz?**  
V: Igen, egy ingyenes próbaverzió letölthető az Aspose weboldaláról.

## Összegzés

Ebben az útmutatóban megtanultuk, hogyan **mentse a OneNote-ot PDF-ként**, miközben a betűkészlet alrendszert vezéreljük Java-ban az Aspose.Note segítségével. A három megközelítés – alapértelmezett betűkészlet név megadása, egyedi betűkészlet fájl betöltése vagy betűkészlet adatfolyam használata – követésével biztosítható a betűkészlet egységes megjelenése a platformok között a OneNote dokumentumok exportálásakor vagy mentésekor.

---

**Legutóbb frissítve:** 2025-12-18  
**Tesztelve:** Aspose.Note for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}