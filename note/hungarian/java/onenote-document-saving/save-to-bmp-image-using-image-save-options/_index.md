---
date: 2025-12-16
description: Tanulja meg, hogyan menthet OneNote dokumentumokat BMP képekbe az Aspose.Note
  for Java kép mentési beállításainak használatával. Továbbá nézze meg, hogyan menthet
  OneNote-ot PDF vagy PNG formátumba.
linktitle: how to save onenote to BMP Image Using Image Save Options
second_title: Aspose.Note Java API
title: Hogyan mentse a OneNote-ot BMP képre a Kép mentési beállítások használatával
url: /hu/java/onenote-document-saving/save-to-bmp-image-using-image-save-options/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# hogyan mentse a onenote BMP képet az Image Save Options használatával

## Introduction

Az Aspose.Note for Java egy erőteljes könyvtár, amely lehetővé teszi a Java fejlesztők számára, hogy programozott módon dolgozzanak a Microsoft OneNote fájlokkal. **Ebben az útmutatóban megtanulja, hogyan mentse a onenote dokumentumokat BMP képekbe** az Aspose.Note for Java Image Save Options funkciójának segítségével. Lépésről lépésre végigvezetjük, elmagyarázzuk, miért választhatja a BMP-et más formátumok helyett, és megmutatjuk, hogyan integrálhatja ezt a képességet saját alkalmazásaiba.

## Quick Answers
- **What does the Image Save Options class do?** It lets you specify the output image format (BMP, PNG, JPEG, etc.) when converting a OneNote page.  
- **Do I need a license to run the sample?** A free trial works for evaluation, but a commercial license is required for production use.  
- **Can I convert a OneNote page to PDF or PNG instead of BMP?** Yes – simply change the `SaveFormat` enum (e.g., `SaveFormat.Pdf` or `SaveFormat.Png`).  
- **Which Java version is supported?** Java 8 and later are fully supported.  
- **Is there any special handling for large documents?** You can stream the output to avoid high memory consumption.

## What is “Image Save Options” in Aspose.Note?
Az `ImageSaveOptions` osztály finomhangolt vezérlést biztosít arról, hogyan renderelődik a OneNote oldal raszteres képként. Beállíthatja a képformátumot, felbontást, színmélységet és még sok mást. Ez a rugalmasság megkönnyíti BMP fájlok generálását régi rendszerekhez vagy PNG/JPEG fájlok létrehozását webes felhasználáshoz.

## Prerequisites

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik a következőkkel:

1. Alapvető ismeretek a Java programozási nyelvről.  
2. JDK (Java Development Kit) telepítve van a gépén.  
3. Egy IDE, például Eclipse vagy IntelliJ IDEA.  
4. Aspose.Note for Java könyvtár – töltse le [itt](https://releases.aspose.com/note/java/).

## Import Packages

Először importálja a szükséges Aspose.Note osztályokat és a standard Java I/O segédeszközöket:

```java
import com.aspose.note.*;
import java.io.IOException;
```

## Step 1: Load the OneNote Document

```java
// The path to the documents directory.
String dataDir = "Your Document Directory";

// Load the document into Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

Itt a forrás OneNote fájlt (`Aspose.one`) tartalmazó mappára mutatunk, és betöltjük egy `Document` objektumba. Ez az objektum teljes hozzáférést biztosít az oldalakhoz, szekciókhoz és egyéb elemekhez a jegyzetfüzetben.

## Step 2: Save the Document as a BMP Image

```java
dataDir = dataDir + "SaveToBmpImageUsingImageSaveOptions_out.bmp";

// Save the document.
oneFile.save(dataDir, new ImageSaveOptions(SaveFormat.Bmp));
```

Összefűzzük a kimeneti fájl nevét, majd meghívjuk a `save` metódust egy `ImageSaveOptions` példánnyal, amely **BMP**-re (`SaveFormat.Bmp`) van konfigurálva.  
Ha **PNG**-ként szeretné menteni a onenote oldalt, egyszerűen cserélje le a `SaveFormat.Bmp`-et `SaveFormat.Png`-re. Hasonlóan, a `SaveFormat.Pdf` lehetővé teszi az **onenote to pdf** konverziót.

## Why Choose BMP?
- **Lossless quality** – BMP stores raw pixel data, preserving the exact appearance of the original page.  
- **Compatibility** – Older Windows applications often require BMP files.  
- **Simplicity** – No compression artifacts, making it ideal for further image processing.

## Common Issues & Tips

- **File path errors** – Ensure `dataDir` ends with the appropriate file separator (`/` or `\`).  
- **Large notebooks** – For very large OneNote files, consider saving each page individually to keep memory usage low.  
- **License exceptions** – Running the code without a valid license will add a watermark to the generated image.

## Conclusion

Ebben az útmutatóban bemutattuk, **hogyan mentse a onenote** dokumentumokat BMP képekbe az Aspose.Note for Java `ImageSaveOptions` segítségével. A `SaveFormat` enum cseréjével PNG, JPEG, PDF vagy más támogatott formátumok is előállíthatók, így rugalmas módot biztosít a OneNote tartalom exportálására bármely további felhasználási forgatókönyvhöz.

## Frequently Asked Questions

**Q1: Can I save OneNote documents to other image formats besides BMP?**  
A: Yes, you can use `ImageSaveOptions` with `SaveFormat.Png`, `SaveFormat.Jpeg`, `SaveFormat.Gif`, or `SaveFormat.Tiff` to export to those formats.

**Q2: Does Aspose.Note for Java support conversion between different document formats?**  
A: Absolutely. Besides image formats, you can convert OneNote files to PDF, DOCX, HTML, and more using the appropriate `SaveFormat`.

**Q3: Is Aspose.Note for Java compatible with the latest versions of OneNote?**  
A: Yes, the library is regularly updated to stay in sync with the newest OneNote releases.

**Q4: Can I manipulate the content of OneNote documents programmatically?**  
A: Yes, you can add, edit, or delete pages, sections, and rich content (text, images, tables) through the API.

**Q5: Does Aspose.Note for Java provide technical support?**  
A: Yes, Aspose offers technical support and a dedicated forum. Visit the [Aspose.Note forum](https://forum.aspose.com/c/note/28) for assistance.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-16  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

---