---
title: Jegyzetfüzet konvertálása lapított képpé a OneNote-ban – Aspose.Note
linktitle: Jegyzetfüzet konvertálása lapított képpé a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan alakíthat át egy jegyzetfüzetet lapos képpé a OneNote-ban az Aspose.Note for Java használatával. Könnyedén megőrizheti az összes elemet egyetlen képfájlban.
weight: 13
url: /hu/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jegyzetfüzet konvertálása lapított képpé a OneNote-ban – Aspose.Note

## Bevezetés

Ebben az oktatóanyagban végigvezetjük a jegyzetfüzet egy lapított képpé alakításán a OneNote alkalmazásban az Aspose.Note for Java használatával. Ez lehetővé teszi a jegyzetfüzet képfájlként történő mentését, biztosítva, hogy minden elem egyetlen képformátumban maradjon meg.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

1. Java Development Kit (JDK) telepítve a rendszerére.
2.  Aspose.Note for Java könyvtár letöltve és beállítva a Java projektben. A könyvtárat innen töltheti le[itt](https://releases.aspose.com/note/java/).
3. Java programozási alapismeretek.

## Csomagok importálása

A kezdéshez importálnia kell a szükséges csomagokat az Aspose.Note for Java-ból:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1. lépés: Állítsa be a dokumentumkönyvtárat

Először is határozza meg a könyvtárat, ahol a jegyzetfüzet fájlja található:

```java
String dataDir = "Your Document Directory";
```

 Cserélje ki`"Your Document Directory"` a jegyzetfüzet fájl elérési útjával.

## 2. lépés: Töltse be a notebookot

 Ezután töltse be a notebook fájlt a`Notebook` osztály:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Biztosítsa a cserét`"test.onetoc2"` a jegyzetfüzet fájl nevével.

## 3. lépés: Állítsa be a képmentési beállításokat

Most állítsa be a jegyzetfüzet képként való mentésére vonatkozó beállításokat. A mentési formátumot PNG-ként adjuk meg, és a felbontást 400 DPI-re állítjuk:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

A felbontást igény szerint állíthatja be.

## 4. lépés: Lapítsa ki a jegyzetfüzetet

Annak érdekében, hogy az összes elemet egyetlen képpé simítsa, állítsa be a`flatten` opciót`true`:

```java
saveOptions.setFlatten(true);
```

Ez biztosítja, hogy az eredményül kapott kép megtartsa a notebook elrendezését.

## 5. lépés: Kép mentése

Végül mentse el a jegyzetfüzetet lapított képként:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Cserélje ki`"ExportImageasFlattenedNotebook_out.png"` a kívánt kimeneti fájlnévvel.

## Következtetés

Összefoglalva, az Aspose.Note for Java használatával könnyedén konvertálhatja jegyzetfüzetét lapos képpé a OneNote-ban. Ez a folyamat biztosítja, hogy minden elem egyetlen képformátumban maradjon meg, megkönnyítve a megosztást és a megtekintést.

## GYIK

### 1. kérdés: Beállíthatom a kimeneti kép felbontását?

 V1: Igen, a felbontást igényei szerint módosíthatja a`setResolution` metódus paraméter.

### 2. kérdés: Az Aspose.Note támogat más képformátumokat az exportáláshoz?

2. válasz: Igen, az Aspose.Note különféle képformátumokat támogat, például PNG, JPEG, BMP stb. a notebookok exportálásához.

### 3. kérdés: Testreszabhatom a kimeneti képet?

3. válasz: Igen, az Aspose.Note széles körű lehetőségeket kínál a kimeneti kép testreszabásához, beleértve az oldalméretet, a tájolást és a minőségi beállításokat.

### 4. kérdés: Elérhető az Aspose.Note for Java próbaverziója?

 4. válasz: Igen, beszerezhet egy ingyenes próbaverziót a webhelyről[itt](https://releases.aspose.com/).

### 5. kérdés: Hol találok támogatást az Aspose.Note for Java számára?

 5. válasz: Támogatást és forrásokat találhat az Aspose.Note fórumon[itt](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
