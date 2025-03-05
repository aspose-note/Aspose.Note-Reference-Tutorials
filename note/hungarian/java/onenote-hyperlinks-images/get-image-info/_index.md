---
title: Képadatok beszerzése a OneNote-ból Java használatával
linktitle: Képadatok beszerzése a OneNote-ból Java használatával
second_title: Aspose.Note Java API
description: Képadatok kibontása a OneNote-dokumentumokból Java nyelven! Képméretek, fájlnevek stb. Könnyű lépéseket és kódpéldákat tartalmaz. #OneNote #Java #Aspose
type: docs
weight: 15
url: /hu/java/onenote-hyperlinks-images/get-image-info/
---
## Bevezetés

A Java fejlesztés területén gyakori feladat az információk kinyerése a különböző dokumentumformátumokból. A OneNote, a jegyzetkészítés népszerű platformja, gyakran tartalmaz képeket a szöveg mellett. A képadatok programozott lekérése a OneNote-fájlokból Java használatával leegyszerűsítheti a dokumentumfeldolgozási munkafolyamatokat. Ebben az oktatóanyagban megvizsgáljuk, hogyan lehet képrészleteket kinyerni a OneNote-dokumentumokból az Aspose.Note for Java használatával.

## Előfeltételek

Mielőtt belemerülnénk a megvalósításba, győződjön meg arról, hogy a következő előfeltételekkel rendelkezik:

### 1. Java fejlesztőkészlet (JDK)

Győződjön meg arról, hogy a Java Development Kit (JDK) telepítve van a rendszeren. Letöltheti és telepítheti a legújabb JDK-t a webhelyről[Oracle webhely](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html).

### 2. Aspose.Note for Java Library

 Töltse le és foglalja bele a projektbe az Aspose.Note for Java könyvtárat. A könyvtárat beszerezheti a[letöltési oldal](https://releases.aspose.com/note/java/).

### 3. OneNote-dokumentum

Készítsen egy minta OneNote-dokumentumot, amely képeket tartalmaz. Ez a dokumentum a képadatok programozott kinyerésére szolgál.

## Csomagok importálása

Kezdésként importálja a szükséges csomagokat az Aspose.Note for Java-ból:

```java
import java.io.IOException;
import java.util.List;
import com.aspose.note.Document;
import com.aspose.note.Image;
```

Bontsuk fel a fenti kódot lépésről lépésre:

## 1. lépés: Állítsa be a dokumentumkönyvtárat

```java
String dataDir = "Your Document Directory";
```

 Cserélje ki`"Your Document Directory"` a OneNote-dokumentum elérési útjával.

## 2. lépés: Töltse be a dokumentumot

```java
Document doc = new Document(dataDir + "Sample1.one");
```

Töltse be a OneNote-dokumentumot az Aspose.Note for Java könyvtár használatával. Győződjön meg róla, hogy a megfelelő elérési utat adta meg a dokumentumhoz.

## 3. lépés: Töltse le az összes képet

```java
List<Image> list = doc.getChildNodes(Image.class);
```

Az összes kép lekérése a betöltött OneNote-dokumentumból.

## 4. lépés: Nyomtassa ki az Összes képszámot

```java
System.out.printf("Total Images: %s\n\n", list.size());
```

Nyomtassa ki a dokumentumban talált képek teljes számát.

## 5. lépés: Bejárás és képinformációk nyomtatása

```java
for (Image image : list) {
    System.out.println("Width: " + image.getWidth());
    System.out.println("Height: " + image.getHeight());
    System.out.println("OriginalWidth: " + image.getOriginalWidth());
    System.out.println("OriginalHeight: " + image.getOriginalHeight());
    System.out.println("FileName: " + image.getFileName());
    System.out.println("LastModifiedTime: " + image.getLastModifiedTime());
    System.out.println();
}
```

Iterálhatja a képek listáját, és nyomtathat olyan részleteket, mint a szélesség, magasság, eredeti méretek, fájlnév és az egyes képek utolsó módosításának ideje.

## Következtetés

Az oktatóanyagban ismertetett lépések követésével hatékonyan lekérheti a képadatokat a OneNote-dokumentumokból Java használatával az Aspose.Note for Java könyvtár segítségével. Ennek a funkciónak az alkalmazásaiba integrálása automatizálhatja a dokumentumfeldolgozással kapcsolatos feladatokat, növelve a hatékonyságot és a termelékenységet.

## GYIK

### 1. kérdés: Az Aspose.Note for Java kezelhet más dokumentumformátumokat a OneNote-on kívül?

1. válasz: Igen, az Aspose.Note for Java különféle dokumentumformátumokat támogat, beleértve a OneNote-ot, a PDF-et és a Microsoft Word-t.

### 2. kérdés: Az Aspose.Note for Java alkalmas személyes és kereskedelmi használatra is?

2. válasz: Igen, az Aspose.Note for Java személyes és kereskedelmi célokra is használható.

### 3. kérdés: Az Aspose.Note for Java technikai támogatást kínál?

 3. válasz: Igen, a technikai támogatás elérhető az Aspose fórumain keresztül a címen[itt](https://forum.aspose.com/c/note/28).

### 4. kérdés: Kipróbálhatom az Aspose.Note for Java programot vásárlás előtt?

 4. válasz: Igen, felfedezheti az Aspose.Note a Java számára ingyenes próbaverzióját[Aspose.Note for Java](https://releases.aspose.com/note/java/).

### 5. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java számára?
 
 V5: Ideiglenes licencet szerezhet be[Ideiglenes jogosítvány/](https://purchase.aspose.com/temporary-license/).