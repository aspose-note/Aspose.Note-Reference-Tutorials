---
title: Képek kibontása a OneNote-dokumentumból Java segítségével
linktitle: Képek kibontása a OneNote-dokumentumból Java segítségével
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan bonthat ki képeket OneNote-dokumentumokból Java használatával az Aspose.Note könyvtárral. Kövesse lépésről lépésre útmutatónkat a zökkenőmentes képkivonáshoz.
weight: 14
url: /hu/java/onenote-hyperlinks-images/extract-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Képek kibontása a OneNote-dokumentumból Java segítségével

## Bevezetés

Ebben az oktatóanyagban végigvezetjük a OneNote-dokumentumból a képek Java használatával az Aspose.Note könyvtár segítségével történő kinyerésének folyamatán.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik az alábbiakkal:

1.  Java Development Kit (JDK): Győződjön meg arról, hogy a Java telepítve van a rendszeren. Letöltheti és telepítheti a[weboldal](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

2.  Aspose.Note könyvtár: Töltse le és foglalja bele az Aspose.Note könyvtárat a Java projektbe. Beszerezheti a[letöltési link](https://releases.aspose.com/note/java/).

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat:

```java
import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Paths;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

## 1. lépés: Töltse be a dokumentumot

Először töltse be a OneNote dokumentumot az Aspose segítségével.Note:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

## 2. lépés: Töltse le az összes képet

Ezután töltse le az összes képet a dokumentumból:

```java
List<Image> list = doc.getChildNodes(Image.class);
System.out.printf("Total Images: %s\n\n", list.size());
```

## 3. lépés: Képek kibontása

Ismételje meg a képek listáját, és mentse az egyes képeket egy fájlba:

```java
for (int i = 0; i < list.size(); i++) {
    Image image = list.get(i);
    String outputFile = "ExtractImages_out" + i + "_" + image.getFileName();
    byte[] buffer = image.getBytes();
    Files.write(Paths.get(dataDir + outputFile), buffer);
    System.out.printf("File saved: %s\n", dataDir);
}
```

## Következtetés

Az Aspose.Note könyvtárral zökkenőmentesen kinyerheti a képeket egy OneNote-dokumentumból Java használatával. Az ebben az oktatóanyagban ismertetett lépések követésével könnyedén lekérheti a képeket a dokumentumokból további feldolgozás vagy elemzés céljából.

## GYIK

### 1. kérdés: Kibonthatok képeket a jelszóval védett OneNote-dokumentumokból?

1. válasz: Igen, az Aspose.Note támogatja a képek kinyerését a jelszóval védett dokumentumokból is.

### 2. kérdés: Az Aspose.Note kompatibilis a Java különböző verzióival?

2. válasz: Az Aspose.Note kompatibilis a Java különféle verzióival, rugalmasságot biztosítva a fejlesztők számára.

### 3. kérdés: Kivonhatok képeket több OneNote-dokumentumból egyetlen végrehajtással?

3. válasz: Természetesen az Aspose.Note segítségével több dokumentumot is végigjárhat, és mindegyikből képeket nyerhet ki.

### 4. kérdés: Vannak méretkorlátozások a OneNote-dokumentumokra vonatkozóan?

A4: Az Aspose.Note hatékonyan kezeli a különböző méretű dokumentumokat, így nem korlátozza a dokumentumok méretét a képkivonáshoz.

### 5. kérdés: Az Aspose.Note támogatja a képeken kívül más típusú tartalom kinyerését?

5. válasz: Igen, a képek mellett az Aspose.Note lehetővé teszi a szövegek, mellékletek és egyéb tartalomtípusok kinyerését a OneNote-dokumentumokból.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
