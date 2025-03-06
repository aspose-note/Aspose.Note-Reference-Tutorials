---
title: Szövegcsomópont hozzáadása címkével a OneNote-ban – Aspose.Note
linktitle: Szövegcsomópont hozzáadása címkével a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Fedezze fel, hogyan adhat hozzá szöveges csomópontokat címkékkel a OneNote-ban az Aspose.Note for Java használatával. Egyszerű, hatékony és fejlesztőbarát. Töltse le a könyvtárat most!
weight: 13
url: /hu/java/onenote-tag-operations/add-text-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Szövegcsomópont hozzáadása címkével a OneNote-ban – Aspose.Note

## Bevezetés
Ebben az oktatóanyagban megvizsgáljuk, hogyan adhatunk hozzá szöveges csomópontot címkével a OneNote-ban az Aspose.Note for Java használatával. Az Aspose.Note egy hatékony Java-könyvtár, amely lehetővé teszi a fejlesztők számára, hogy programozottan dolgozzanak Microsoft OneNote fájlokkal. A szöveges csomópontok címkékkel való hozzáadása gyakori követelmény a dokumentumfeldolgozás során, és az Aspose.Note leegyszerűsíti ezt a feladatot.
## Előfeltételek
Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
- Java programozási alapismeretek.
-  Aspose.Note for Java könyvtár telepítve. Letöltheti[itt](https://releases.aspose.com/note/java/).
- Java fejlesztéshez beállított integrált fejlesztői környezet (IDE).
## Csomagok importálása
Kezdje a Java-projekthez szükséges csomagok importálásával. A kódba foglalja bele a következő importálásokat:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
## 1. lépés: Hozzon létre dokumentumobjektumot
Inicializáljon egy dokumentum osztály objektumot a OneNote-dokumentum megjelenítéséhez:
```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory";
//Hozzon létre egy objektumot a Dokumentum osztályból
Document doc = new Document();
```
## 2. lépés: Az oldalosztály objektum inicializálása
Inicializáljon egy oldalosztály objektumot, hogy az oldalt a dokumentumban képviselje:
```java
// Oldal osztály objektum inicializálása
Page page = new Page();
```
## 3. lépés: Inicializálja az Outline osztály objektumot
Inicializáljon egy Outline osztályobjektumot az oldalon belüli tartalom strukturálásához:
```java
// Inicializálja az Outline osztály objektumot
Outline outline = new Outline();
```
## 4. lépés: Inicializálja az OutlineElement osztályobjektumot
Inicializáljon egy OutlineElement osztályobjektumot, hogy egy elemet képviseljen a vázlaton belül:
```java
// Inicializálja az OutlineElement osztályobjektumot
OutlineElement outlineElem = new OutlineElement();
```
## 5. lépés: A szövegstílus testreszabása
Állítsa be a szövegcsomópont stílusát, például betűszínt, nevet és méretet:
```java
// A szövegstílus testreszabása
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```
## 6. lépés: Hozzon létre RichText objektumot
Hozzon létre egy RichText objektumot, és fűzze hozzá a kívánt szöveget:
```java
// Hozzon létre RichText objektumot
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```
## 7. lépés: Adjon hozzá megjegyzéscímkét
Adjon hozzá megjegyzéscímkét, például sárga csillagot a szöveghez:
```java
// Jegyzetcímke hozzáadása
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
## 8. lépés: Szövegcsomópont hozzáadása
Adja hozzá a szöveges csomópontot a vázlat elemhez:
```java
// Szöveg csomópont hozzáadása
outlineElem.appendChildLast(text);
```
## 9. lépés: Adja hozzá az Outline elemet az Outlinehoz
Adja hozzá a vázlat elemet a vázlathoz:
```java
// Vázlatelem csomópont hozzáadása
outline.appendChildLast(outlineElem);
```
## 10. lépés: Vázlat hozzáadása az oldalhoz
Adja hozzá a vázlatot az oldalhoz:
```java
// Vázlat csomópont hozzáadása
page.appendChildLast(outline);
```
## 11. lépés: Oldal hozzáadása a dokumentumhoz
Az oldal hozzáadása a dokumentumhoz:
```java
// Oldalcsomópont hozzáadása
doc.appendChildLast(page);
```
## 12. lépés: Mentse el a OneNote-dokumentumot
Mentse a OneNote-dokumentumot a megadott könyvtárba:
```java
// Mentse a OneNote-dokumentumot
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```
Gratulálunk! Sikeresen hozzáadott egy szöveges csomópontot címkével a OneNote-ban az Aspose.Note for Java használatával.
## Következtetés
Ebben az oktatóanyagban lépésről lépésre bemutattuk egy szöveges csomópont címkével történő hozzáadásának folyamatát a OneNote-ban az Aspose.Note for Java könyvtár használatával. Ez a hatékony könyvtár leegyszerűsíti a dokumentumfeldolgozási feladatokat, és megkönnyíti a fejlesztők számára a OneNote-fájlok programozott kezelését.
## Gyakran Ismételt Kérdések
### K: Használhatom az Aspose.Note for Java programot más Java könyvtárakkal?
V: Igen, az Aspose.Note for Java zökkenőmentesen integrálható más Java-könyvtárakba a dokumentumfeldolgozási képességek javítása érdekében.
### K: Elérhető az Aspose.Note for Java ingyenes próbaverziója?
 V: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).
### K: Hogyan kaphatok támogatást az Aspose.Note for Java számára?
V: Kérhet támogatást az Aspose.Note közösségtől[fórum](https://forum.aspose.com/c/note/28).
### K: Rendelkezésre állnak ideiglenes licencek az Aspose.Note for Java számára?
 V: Igen, beszerezhet ideiglenes engedélyeket[itt](https://purchase.aspose.com/temporary-license/).
### K: Hol találom az Aspose.Note for Java dokumentációját?
 V: A dokumentáció elérhető[itt](https://reference.aspose.com/note/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
