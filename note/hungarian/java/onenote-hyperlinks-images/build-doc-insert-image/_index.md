---
title: Dokumentum létrehozása és kép beszúrása a OneNote-ba Java használatával
linktitle: Dokumentum létrehozása és kép beszúrása a OneNote-ba Java használatával
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan hozhat létre OneNote-dokumentumokat és szúrhat be képeket az Aspose.Note for Java használatával. Lépésről lépésre bemutató útmutató a zökkenőmentes integrációhoz.
type: docs
weight: 12
url: /hu/java/onenote-hyperlinks-images/build-doc-insert-image/
---
## Bevezetés

Ebben az oktatóanyagban megvizsgáljuk, hogyan használható az Aspose.Note for Java OneNote-dokumentumok létrehozásához és képek beillesztéséhez. Az Aspose.Note egy hatékony Java API, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft OneNote fájlokkal. Az egyes lépéseket részletesen lebontjuk, hogy végigvezetjük a folyamaton.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren.
2.  Aspose.Note for Java könyvtár: Töltse le és telepítse az Aspose.Note for Java könyvtárat a[weboldal](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment): Használjon bármilyen Java által támogatott IDE-t, például az IntelliJ IDEA-t vagy az Eclipse-t a kódoláshoz.

## Csomagok importálása

Kezdje a szükséges csomagok importálásával a Java kódban:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

## 1. lépés: Állítsa be a dokumentumot

Először hozzon létre egy új OneNote-dokumentumot, és inicializálja a szükséges objektumokat:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 2. lépés: Inicializálja az Outline-t

Állítsa be a dokumentum vázlatát, és adja meg az eltolás tulajdonságait:

```java
Outline outline = new Outline();
outline.setVerticalOffset(0);
outline.setHorizontalOffset(0);
```

## 3. lépés: Kép hozzáadása

Töltse be a képet, és adja meg az igazítását:

```java
Image image = new Image(null, dataDir + "Input.jpg");
image.setAlignment(HorizontalAlignment.Right);
```

## 4. lépés: Kép hozzáadása a körvonalelemhez

A kép csatolása egy körvonalelemhez:

```java
OutlineElement outlineElem = new OutlineElement();
outlineElem.appendChildLast(image);
```

## 5. lépés: Vázlat és oldalcsomópontok hozzáadása

Adja hozzá a vázlatot és az oldalcsomópontokat a dokumentumhoz:

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 6. lépés: Mentse el a dokumentumot

Végül mentse a OneNote-dokumentumot:

```java
try {
    doc.save(dataDir + "NewOneNotedocument_out", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan hozhat létre OneNote-dokumentumokat, és hogyan szúrhat be képeket az Aspose.Note for Java segítségével. Az alábbi lépések követésével hatékonyan kezelheti és kezelheti a OneNote-fájlokat a Java-alkalmazásokban.

## GYIK

### 1. kérdés: Hol találom az Aspose.Note for Java dokumentációját?

 V1: Hozzáférhet a dokumentációhoz[itt](https://reference.aspose.com/note/java/).

### 2. kérdés: Hogyan tölthetem le az Aspose.Note-ot Java-hoz?

 2. válasz: Az Aspose.Note for Java letölthető innen[letöltési oldal](https://releases.aspose.com/note/java/).

### 3. kérdés: Elérhető az Aspose.Note for Java ingyenes próbaverziója?

 V3: Igen, ingyenes próbaverziót kaphat a[weboldal](https://releases.aspose.com/).

### 4. kérdés: Hol kaphatok támogatást az Aspose.Note for Java számára?

 A4: Támogatásért keresse fel a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).

### 5. kérdés: Kaphatok ideiglenes licencet az Aspose.Note for Java számára?

 V5: Igen, kérhet ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).
