---
title: Állítsa be az alapértelmezett bekezdésstílust a OneNote-ban – Aspose.Note
linktitle: Állítsa be az alapértelmezett bekezdésstílust a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan állíthat be alapértelmezett bekezdésstílusokat a OneNote-ban az Aspose.Note for Java használatával. Kövesse lépésenkénti útmutatónkat a Java-alkalmazások hatékony szövegformázásához.
weight: 11
url: /hu/java/onenote-styles/set-default-paragraph-style/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Állítsa be az alapértelmezett bekezdésstílust a OneNote-ban – Aspose.Note

## Bevezetés

Az Aspose.Note for Java hatékony lehetőségeket kínál a szövegformázás manipulálására, beleértve az alapértelmezett bekezdésstílusok beállítását. Ez az oktatóanyag végigvezeti az alapértelmezett bekezdésstílusok beállításának folyamatán a OneNote-ban az Aspose.Note használatával.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik az alábbiakkal:

1. Java Development Kit (JDK): Győződjön meg arról, hogy a JDK telepítve van a rendszeren.
2.  Aspose.Note for Java Library: Töltse le és telepítse az Aspose.Note for Java programot a[letöltési oldal](https://releases.aspose.com/note/java/).
3. Integrált fejlesztői környezet (IDE): A kódolás kényelme érdekében telepítenie kell egy IDE-t, például az Eclipse-t vagy az IntelliJ IDEA-t.

## Csomagok importálása

Először is importálja a szükséges csomagokat a kódolás megkezdéséhez:

```java
import com.aspose.note.*;

import java.awt.*;
import java.io.FileInputStream;
import java.io.IOException;
import java.nio.file.Paths;
import java.util.List;
```

Most bontsuk fel a példakódot több lépésre:

## 1. lépés: Inicializálja a dokumentumot, az oldalt és a vázlatot

```java
String dataDir = "Your Document Directory";
Document document = new Document();
Page page = new Page();
Outline outline = new Outline();
```

## 2. lépés: Hozzon létre egy vázlatelemet

```java
OutlineElement outlineElem = new OutlineElement();
```

## 3. lépés: Határozza meg az alapértelmezett bekezdésstílust

```java
ParagraphStyle defaultStyle = new ParagraphStyle()
										.setFontName("Courier New")
										.setFontSize(20);
```

## 4. lépés: Hozzon létre gazdag szöveget az alapértelmezett stílussal

```java
RichText text = new RichText()
					.append("DefaultParagraphFontAndSize")
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFont", new TextStyle().setFontSize(14))
					.append(System.lineSeparator())
					.append("OnlyDefaultParagraphFontSize", new TextStyle().setFontName("Verdana"));
text.setParagraphStyle(defaultStyle);
```

## 5. lépés: Rögzített szöveg hozzáfűzése a vázlatelemhez

```java
outlineElem.appendChildLast(text);
```

## 6. lépés: Csatlakoztassa a Vázlat elemet a Vázlathoz

```java
outline.appendChildLast(outlineElem);
```

## 7. lépés: Vázlat hozzáfűzése az oldalhoz

```java
page.appendChildLast(outline);
```

## 8. lépés: Oldal hozzáfűzése a dokumentumhoz

```java
document.appendChildLast(page);
```

## 9. lépés: Mentse el a dokumentumot

```java
document.save(Paths.get(dataDir, "SetDefaultParagraphStyle.one").toString());
```

Ez a kód beállítja az alapértelmezett bekezdésstílust a OneNote-ban az Aspose.Note for Java használatával.

## Következtetés

Az alapértelmezett bekezdésstílusok programozott beállítása a OneNote-ban hatékonyan megvalósítható az Aspose.Note for Java segítségével. Az oktatóanyagban ismertetett lépések követésével zökkenőmentesen integrálhatja ezt a funkciót Java-alkalmazásaiba.

## GYIK

### 1. kérdés: Testreszabhatom az alapértelmezett bekezdésstílust?

V1: Igen, beállíthat különféle paramétereket, például a betűtípus nevét, méretét, színét és igazítását az igényeinek megfelelően.

### 2. kérdés: Az Aspose.Note támogat más szövegformázási műveleteket?

2. válasz: Az Aspose.Note teljes mértékben támogatja a szöveg formázását, beleértve a betűstílusokat, a felsorolásjeleket és a behúzást.

### 3. kérdés: Az Aspose.Note kompatibilis a OneNote összes verziójával?

3. válasz: Az Aspose.Note-ot úgy tervezték, hogy különböző verziójú Microsoft OneNote-fájlokkal működjön, így széleskörű kompatibilitást biztosít.

### 4. kérdés: Integrálhatom az Aspose.Note-ot a meglévő Java projektembe?

4. válasz: Igen, könnyedén integrálhatja az Aspose.Note-ot Java-projektjeibe a szükséges függőségek hozzáadásával és a szükséges csomagok importálásával.

### 5. kérdés: Elérhető az Aspose.Note próbaverziója?

 5. válasz: Igen, hozzáférhet az Aspose.Note ingyenes próbaverziójához a[weboldal](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
