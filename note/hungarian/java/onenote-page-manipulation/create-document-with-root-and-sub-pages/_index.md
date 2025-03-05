---
title: Hozzon létre dokumentumot gyökér- és aloldalakkal a OneNote-ban
linktitle: Hozzon létre dokumentumot gyökér- és aloldalakkal a OneNote-ban
second_title: Aspose.Note Java API
description: Hozzon létre gyökér- és aloldalakat tartalmazó dokumentumot a OneNote-ban az Aspose.Note for Java segítségével. Kövesse a lépésenkénti útmutatót a jegyzetek hatékony rendszerezéséhez.
type: docs
weight: 11
url: /hu/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---
## Bevezetés

Ebben az oktatóanyagban végigvezetjük a gyökér- és aloldalakat tartalmazó dokumentum létrehozásának folyamatán a OneNote-ban az Aspose.Note for Java használatával. Ha követi ezeket a lépéseket, hatékonyan szervezheti a OneNote-dokumentumokat hierarchikus szerkezettel.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

1. Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren.
2. Aspose.Note for Java: Töltse le és telepítse az Aspose.Note for Java programot a[weboldal](https://purchase.aspose.com/buy).
3. Integrált fejlesztői környezet (IDE): Válasszon Java IDE-t, például IntelliJ IDEA, Eclipse vagy NetBeans.

## Csomagok importálása

Kezdje azzal, hogy importálja a szükséges csomagokat a Java projektbe:

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

## 1. lépés: Állítsa be a dokumentumkönyvtárat

Határozza meg a könyvtárat, ahová menteni szeretné a OneNote-dokumentumot:

```java
String dataDir = "Your Document Directory";
```

## 2. lépés: Hozzon létre dokumentumobjektumot

 Példányosítás a`Document` tárgy:

```java
Document doc = new Document();
```

## 3. lépés: Hozzon létre oldalakat

Az oldalobjektumok inicializálása és szintjeik beállítása:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 4. lépés: Adjon hozzá csomópontokat az oldalakhoz

### Csomópontok hozzáadása az első oldalhoz

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text = new RichText().append("First page.");
text.setParagraphStyle(textStyle);

outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page1.appendChildLast(outline);
```

### Csomópontok hozzáadása a második oldalhoz

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Csomópontok hozzáadása a harmadik oldalhoz

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## 5. lépés: Adjon hozzá oldalakat a dokumentumhoz

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 6. lépés: Mentse el a dokumentumot

Mentse el a OneNote-dokumentumot:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Kivétel kezelése
}
```

Gratulálunk! Sikeresen létrehozott egy gyökér- és aloldalakat tartalmazó dokumentumot a OneNote-ban az Aspose.Note for Java használatával.

## Következtetés

A OneNote-dokumentumok hierarchikus felépítésű rendszerezése elengedhetetlen a jobb kezelés és navigáció érdekében. Az Aspose.Note for Java segítségével hatékonyan hozhat létre gyökér- és aloldalakat tartalmazó dokumentumokat, egyértelmű és szervezett elrendezést biztosítva jegyzetei számára.

## GYIK

### 1. kérdés: Létrehozhatok több szintű aloldalt az Aspose.Note for Java használatával?

1. válasz: Igen, több szintű aloldalt is létrehozhat, ha minden oldalhoz beállítja a megfelelő szintet.

### 2. kérdés: Az Aspose.Note for Java kompatibilis a különböző Java IDE-kkel?

2. válasz: Igen, az Aspose.Note for Java kompatibilis az olyan népszerű Java IDE-kkel, mint az IntelliJ IDEA, az Eclipse és a NetBeans.

### 3. kérdés: Testreszabhatom a szöveg formázását a OneNote-dokumentumban?

3. válasz: Igen, testreszabhatja a betűtípust, a színt, a méretet és az egyéb formázási beállításokat az Aspose.Note for Java rich text szolgáltatásaival.

### 4. kérdés: Az Aspose.Note for Java támogatja a dokumentumok különböző formátumokban történő mentését?

4. válasz: Igen, az Aspose.Note for Java támogatja a dokumentumok mentését különböző formátumokban, beleértve a BMP, PDF, PNG stb.

### 5. kérdés: Elérhető az Aspose.Note for Java próbaverziója?

5. válasz: Igen, letöltheti az Aspose.Note for Java ingyenes próbaverzióját a webhelyről.