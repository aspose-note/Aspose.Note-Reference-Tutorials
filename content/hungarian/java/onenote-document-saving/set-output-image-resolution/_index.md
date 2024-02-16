---
title: A kimeneti képfelbontás beállítása a OneNote-ban – Aspose.Note
linktitle: A kimeneti képfelbontás beállítása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan állíthatja be a képfelbontást a OneNote-dokumentumokban az Aspose.Note for Java segítségével. Kövesse lépésről lépésre útmutatónkat az egyszerű megvalósítás érdekében
type: docs
weight: 23
url: /hu/java/onenote-document-saving/set-output-image-resolution/
---
## Bevezetés

Szeretné manipulálni a képek felbontását a OneNote-dokumentumokban Java segítségével? Az Aspose.Note for Java robusztus megoldást kínál az ilyen feladatokra. Ebben az oktatóanyagban végigvezetjük a kimeneti képfelbontás Aspose.Note segítségével történő beállításának lépéseit.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Java Development Kit (JDK): Telepítse a JDK-t a rendszerére.
2. Aspose.Note for Java: Töltse le és telepítse az Aspose.Note for Java programot a[weboldal](https://releases.aspose.com/note/java/).
3. Integrált fejlesztői környezet (IDE): Válassza ki a kívánt IDE-t, például az Eclipse-t vagy az IntelliJ IDEA-t.

## Csomagok importálása

Java-projektjébe importálja a szükséges Aspose.Note csomagokat:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## 1. lépés: Töltse be a OneNote-dokumentumot

Kezdje azzal, hogy betölti a OneNote dokumentumot a Java alkalmazásba:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Cserélje ki`"Your Document Directory"` azzal a tényleges könyvtárral, amelyben a OneNote-dokumentum található.

## 2. lépés: Állítsa be a képmentési beállításokat

Határozza meg a képmentési beállításokat, és adja meg a kívánt felbontást:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Itt állítjuk be a felbontást`120 dpi`. Ezt az értéket igényei szerint módosíthatja.

## 3. lépés: Mentse el a dokumentumot módosított felbontással

Mentse el a dokumentumot frissített képfelbontással:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Ezzel elmenti a módosított dokumentumot a megadott felbontással.

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk, hogyan állíthatja be a kimeneti képfelbontást a OneNote-dokumentumokban az Aspose.Note for Java használatával. Ezen egyszerű lépések követésével hatékonyan módosíthatja a képek felbontását, hogy megfeleljen az alkalmazás követelményeinek.


## GYIK

### 1. kérdés: Beállíthatom a képfelbontást 120 dpi-nél nagyobb értékre?

V1: Igen, a felbontást bármilyen kívánt értékre állíthatja az igényeinek megfelelően.

### 2. kérdés: Az Aspose.Note támogatja a JPEG-en kívül más képformátumokat is?

2. válasz: Igen, az Aspose.Note különféle képformátumokat támogat, például PNG, BMP, GIF stb.

### 3. kérdés: Az Aspose.Note kompatibilis a Java összes verziójával?

3. válasz: Az Aspose.Note kompatibilis a Java 1.6-os vagy újabb verzióival.

### 4. kérdés: Az Aspose.Note segítségével manipulálhatom a OneNote-dokumentumokban lévő képek egyéb aspektusait?

4. válasz: Igen, az Aspose.Note átfogó funkciókat kínál a képkezeléshez, beleértve az átméretezést, a kivágást és az elforgatást.

### 5. kérdés: Hol kaphatok támogatást az Aspose.Note-tal kapcsolatos lekérdezésekhez?

 5. válasz: Kérhet segítséget az Aspose.Note közösségi fórumtól[itt](https://forum.aspose.com/c/note/28).