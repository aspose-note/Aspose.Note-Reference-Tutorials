---
title: Számozott lista létrehozása a OneNote-ban – Aspose.Note
linktitle: Számozott lista létrehozása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan hozhat létre könnyedén számozott listát a OneNote-ban az Aspose.Note for Java segítségével. Tölts le egy ingyenes próbaverziót, és merülj el a Java fejlesztés világában!
weight: 14
url: /hu/java/onenote-text-manipulation/create-numbered-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Számozott lista létrehozása a OneNote-ban – Aspose.Note

## Bevezetés
Az Aspose.Note for Java lehetővé teszi a Java fejlesztők számára, hogy zökkenőmentesen dolgozzanak a Microsoft OneNote fájlokkal. Ebben az oktatóanyagban végigvezetjük a számozott lista létrehozásának folyamatán a OneNote-ban a hatékony Aspose.Note for Java könyvtárral.
## Előfeltételek
Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:
- Java Development Kit (JDK) telepítése a gépen.
-  Aspose.Note a Java könyvtárhoz letöltve innen[itt](https://releases.aspose.com/note/java/).
## Csomagok importálása
Először is importáljuk a szükséges csomagokat a Java-projektbe, hogy a legtöbbet hozhassuk ki az Aspose.Note funkcióiból. Helyezze be a következő kódot a projektbe:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NumberFormat;
import com.aspose.note.NumberList;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.ParagraphStyle;
```
## 1. lépés: A dokumentum-, oldal- és vázlatobjektumok inicializálása
```java
// Az Ön dokumentumkönyvtára
String dataDir = "Your Document Directory";
// Dokumentum, oldal és körvonal objektumok létrehozása
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
// Állítsa be az alapértelmezett szövegstílust
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
Document doc = new Document();
Page page = new Page();
Outline outline = new Outline();
```
## 2. lépés: Az alapértelmezett szövegstílus beállítása
```java
ParagraphStyle defaultStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);
```
## 3. lépés: Vázlatelemek létrehozása
Most hozzuk létre a számozott lista elemeit.
```java
OutlineElement outlineElem1 = new OutlineElement();
outlineElem1.setNumberList(new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10));
RichText text1 = new RichText().append("First");
text1.setParagraphStyle(defaultStyle);
outlineElem1.appendChildLast(text1);
// Ismételje meg a többi elemhez (outlineElem2 és outlineElem3)
```
## 4. lépés: Vázlatelemek hozzáadása az Outline-hoz
```java
outline.appendChildLast(outlineElem1);
outline.appendChildLast(outlineElem2);
outline.appendChildLast(outlineElem3);
```
## 5. lépés: Vázlat hozzáadása az oldalhoz
```java
page.appendChildLast(outline);
```
## 6. lépés: A dokumentum mentése
```java
doc.appendChildLast(page);
doc.save(dataDir + "CreateNumberedList_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "CreateNumberedList_out.pdf");
```
Kövesse ezeket a lépéseket aprólékosan, és könnyedén létrehozhat egy számozott listát a OneNote-ban az Aspose.Note for Java használatával.
## Következtetés
Ebben az oktatóanyagban azt a zökkenőmentes folyamatot vizsgáltuk meg, amellyel számozott listát hozhatunk létre a OneNote-ban az Aspose.Note for Java használatával. A könyvtár robusztus funkciói felbecsülhetetlen értékű eszközzé teszik a Microsoft OneNote fájlokkal dolgozó Java-fejlesztők számára.
## Gyakran Ismételt Kérdések
### K: Testreszabhatom a számozási formátumot a OneNote-listámban?
V: Abszolút! A számozási formátum testreszabható az Aspose.Note for Java által biztosított NumberList osztály használatával.
### K: Elérhető az Aspose.Note for Java próbaverziója?
 V: Igen, letölthet egy ingyenes próbaverziót[itt](https://releases.aspose.com/).
### K: Hogyan kaphatok támogatást az Aspose.Note for Java számára?
 V: Látogassa meg a[Aspose.Note for Java fórum](https://forum.aspose.com/c/note/28) közösségi támogatásért.
### K: Hol találom az Aspose.Note for Java részletes dokumentációját?
 V: Lásd a[dokumentáció](https://reference.aspose.com/note/java/) átfogó tájékoztatásért.
### K: Hogyan vásárolhatok licencet az Aspose.Note for Java számára?
 V: Vásárolhat licencet[itt](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
