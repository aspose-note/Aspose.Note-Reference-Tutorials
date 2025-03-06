---
title: Hozzon létre OneNote-dokumentumot, és mentse HTML-be – Java
linktitle: Hozzon létre OneNote-dokumentumot, és mentse HTML-be – Java
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan hozhat létre és menthet OneNote-dokumentumokat HTML-ként az Aspose.Note for Java használatával. Integrálható a Java-alkalmazásokba a OneNote programozott fájlkezeléséhez.

weight: 18
url: /hu/java/onenote-document-loading/create-onenote-save-to-html/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hozzon létre OneNote-dokumentumot, és mentse HTML-be – Java

## Bevezetés

Az Aspose.Note for Java egy hatékony könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft OneNote fájlokkal. Ebben az oktatóanyagban megvizsgáljuk, hogyan hozhat létre OneNote-dokumentumot, és hogyan mentheti azt HTML formátumba az Aspose.Note for Java használatával.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

1. Java Development Kit (JDK) telepítve a rendszerére.
2.  Aspose.Note a Java könyvtárhoz. Letöltheti innen[itt](https://releases.aspose.com/note/java/).
3. Java programozási alapismeretek.

## Csomagok importálása

Először importálja a szükséges csomagokat a Java projektbe:

```java
import java.io.ByteArrayOutputStream;
import java.io.File;
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.nio.file.Paths;
import com.aspose.note.CssSavingArgs;
import com.aspose.note.Document;
import com.aspose.note.FontFaceType;
import com.aspose.note.FontSavingArgs;
import com.aspose.note.HtmlSaveOptions;
import com.aspose.note.ICssSavingCallback;
import com.aspose.note.IFontSavingCallback;
import com.aspose.note.IImageSavingCallback;
import com.aspose.note.ImageSavingArgs;
import com.aspose.note.ResourceExportType;
```

## 1. lépés: Hozzon létre egy OneNote-dokumentumobjektumot

```java
Document document = new Document("Path_to_your_sample_one_file");
```

 Ez a kód inicializálja a`Document` objektumot egy minta OneNote-fájl betöltésével.

## 2. lépés: Mentse HTML-ként a Memory Stream-be

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setFontFaceTypes(FontFaceType.Ttf);

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
document.save(outputStream, options);
```

Itt beállítjuk a HTML mentési beállításokat, és elmentjük a dokumentumot egy memóriafolyamba.

## 3. lépés: Mentse el HTML-ként az erőforrásokat külön fájlokban

```java
HtmlSaveOptions options = new HtmlSaveOptions();
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);

document.save("output_directory/document.html", options);
```

Ez a lépés a dokumentumot HTML-ként menti, olyan erőforrásokkal, mint a CSS, a betűtípusok és a képek külön fájlokban.

## 4. lépés: Mentse HTML-ként a memóriafolyamba visszahívásokkal az erőforrások mentéséhez

```java
Document document = new Document("Path_to_your_sample_one_file");

UserSavingCallbacks savingCallbacks = new UserSavingCallbacks();
savingCallbacks.setRootFolder("documentFolder");
savingCallbacks.setCssFolder("css");
savingCallbacks.setKeepCssStreamOpened(true);
savingCallbacks.setImagesFolder("images");
savingCallbacks.setFontsFolder("fonts");

HtmlSaveOptions options = new HtmlSaveOptions();
options.setFontFaceTypes(FontFaceType.Ttf);
options.setCssSavingCallback(savingCallbacks);
options.setImageSavingCallback(savingCallbacks);
options.setFontSavingCallback(savingCallbacks);
options.setExportCss(ResourceExportType.ExportEmbedded);
options.setExportImages(ResourceExportType.ExportEmbedded);
options.setExportFonts(ResourceExportType.ExportEmbedded);

File dir = new File(savingCallbacks.getRootFolder());
if (!dir.exists()) {
    dir.mkdir();
}

document.save(Paths.get(savingCallbacks.getRootFolder(), "document.html").toString(), options);
```

Itt HTML-ként mentjük a dokumentumot egy memóriafolyamba, visszahívások segítségével az erőforrás-megtakarítás kezeléséhez.

## Következtetés

Gratulálunk! Megtanulta, hogyan lehet OneNote-dokumentumot létrehozni és HTML formátumba menteni az Aspose.Note for Java használatával. Most már integrálhatja ezt a funkciót Java-alkalmazásaiba, hogy programozottan dolgozhasson a OneNote-fájlokkal.

## GYIK

### 1. kérdés: Konvertálhatok egyszerre több OneNote-dokumentumot HTML-formátumba?

1. válasz: Igen, végignézhet több dokumentumon, és iteratív módon alkalmazhatja a mentési folyamatot.

### 2. kérdés: Az Aspose.Note for Java támogatja a HTML-en kívül más kimeneti formátumokat is?

2. válasz: Igen, az Aspose.Note for Java különféle kimeneti formátumokat támogat, beleértve a PDF-, DOCX- és képformátumokat.

### 3. kérdés: Elérhető az Aspose.Note for Java próbaverziója?

3. válasz: Igen, letölthet egy ingyenes próbaverziót a webhelyről[itt](https://releases.aspose.com/).

### 4. kérdés: Hol kaphatok támogatást az Aspose.Note for Java számára?

 A4: Támogatást kaphat a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).

### 5. kérdés: Hogyan vásárolhatok licencet az Aspose.Note for Java számára?

 5. válasz: Licenceket vásárolhat a[Aspose honlapja](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
