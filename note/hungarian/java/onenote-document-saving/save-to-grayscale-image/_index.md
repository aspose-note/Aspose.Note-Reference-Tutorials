---
title: Mentés szürkeárnyalatos képbe a OneNote-ban – Aspose.Note
linktitle: Mentés szürkeárnyalatos képbe a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan menthet el egy dokumentumot szürkeárnyalatos képként a OneNote-ban az Aspose.Note for Java használatával. A Microsoft OneNote dokumentumokat egyszerűen, programozottan kezelheti.
type: docs
weight: 17
url: /hu/java/onenote-document-saving/save-to-grayscale-image/
---
## Bevezetés

Ebben az oktatóanyagban megvizsgáljuk, hogyan lehet egy dokumentumot szürkeárnyalatos képként menteni a OneNote-ban az Aspose.Note for Java használatával. A szürkeárnyalatos képek monokromatikus képek, ahol a színinformációkat csak a szürke árnyalatai képviselik. Az Aspose.Note egy hatékony Java API, amely lehetővé teszi a Microsoft OneNote dokumentumok programozott kezelését.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

1. Java Development Kit (JDK) telepítve a rendszerére.
2.  Aspose.Note a Java könyvtárhoz. Letöltheti innen[itt](https://releases.aspose.com/note/java/).
3. A Java programozás alapvető ismerete.

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## 1. lépés: Töltse be a dokumentumot

 Először töltse be a dokumentumot az Aspose.Note-ba. Cserélje ki`"Your Document Directory"` a dokumentumkönyvtár elérési útjával és`"Aspose.one"` a OneNote-dokumentum nevével.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## 2. lépés: Állítsa be a kimeneti útvonalat és az opciókat

Határozza meg a szürkeárnyalatos kép kimeneti útvonalát, és adja meg a mentési beállításokat. A színmódot szürkeárnyalatosra állítjuk.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## 3. lépés: Mentse el a dokumentumot

Végül mentse a dokumentumot szürkeárnyalatos képként a megadott beállításokkal.

```java
oneFile.save(dataDir, options);
```

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan lehet egy dokumentumot szürkeárnyalatos képként menteni a OneNote-ban az Aspose.Note for Java használatával. Ez hihetetlenül hasznos lehet különböző alkalmazásokban, ahol szürkeárnyalatos képekre van szükség.

## GYIK

### 1. kérdés: Elmenthetem a szürkeárnyalatos képet más formátumban?

 A1: Igen, megteheti. Egyszerűen változtassa meg a`SaveFormat` paraméter a`ImageSaveOptions` konstruktor a kívánt formátumra.

### 2. kérdés: Az Aspose.Note kompatibilis a OneNote-dokumentumok összes verziójával?

2. válasz: Az Aspose.Note támogatja a Microsoft OneNote 2010 és újabb verzióit.

### 3. kérdés: Az Aspose.Note használatához licenc szükséges?

3. válasz: Igen, az Aspose.Note éles környezetben való használatához érvényes licenc szükséges. Tesztelési célra azonban ideiglenes licencet szerezhet.

### 4. kérdés: Módosíthatom a dokumentum egyéb aspektusait, mielőtt képként elmenteném?

A4: Abszolút! Az Aspose.Note szolgáltatások széles skáláját kínálja a OneNote-dokumentumok programozott szerkesztéséhez.

### 5. kérdés: Hol találok támogatást, ha problémákba ütközöm?

5. válasz: Támogatást találhat az Aspose.Note fórumon[itt](https://forum.aspose.com/c/note/28).