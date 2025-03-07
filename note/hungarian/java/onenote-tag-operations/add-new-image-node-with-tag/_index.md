---
title: Új képcsomópont hozzáadása címkével a OneNote-ban – Aspose.Note
linktitle: Új képcsomópont hozzáadása címkével a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Ismerje meg, hogyan adhat hozzá új képcsomópontot címkével a OneNote-ban az Aspose.Note for Java használatával. Fejlessze Java programozási készségeit könnyedén.
weight: 10
url: /hu/java/onenote-tag-operations/add-new-image-node-with-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Új képcsomópont hozzáadása címkével a OneNote-ban – Aspose.Note

## Bevezetés
Java programozás területén az Aspose.Note hatékony eszköz a OneNote dokumentumok egyszerű kezeléséhez. Ha fejleszteni szeretné készségeit, és megtanulja, hogyan adhat hozzá új képcsomópontot címkével a OneNote-ban az Aspose.Note segítségével, akkor jó helyen jár. Ez a lépésenkénti útmutató végigvezeti Önt a folyamaton, biztosítva, hogy minden koncepciót alaposan megértsen.
## Előfeltételek
Mielőtt belevágnánk az oktatóanyagba, győződjünk meg arról, hogy mindennel rendelkezik, amire szüksége van:
1.  Aspose.Note Java esetén: Győződjön meg arról, hogy telepítve van az Aspose.Note könyvtár. Ha nem, akkor letöltheti[itt](https://releases.aspose.com/note/java/).
2. Java fejlesztői környezet: Győződjön meg arról, hogy működő Java fejlesztői környezet van beállítva a gépén.
Most, hogy megvannak az előfeltételek, folytassuk a következő lépésekkel.
## Csomagok importálása
Java projektjében kezdje a szükséges csomagok importálásával:
```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Image;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
```
## 1. lépés: Hozzon létre dokumentumobjektumot
```java
// A dokumentumok könyvtárának elérési útja.
String dataDir = "Your Document Directory";
// hozzon létre egy objektumot a Dokumentum osztályból
Document doc = new Document();
```
## 2. lépés: Az oldalosztály objektum inicializálása
```java
// inicializálja az oldalosztály objektumot
Page page = new Page();
```
## 3. lépés: Inicializálja az Outline osztály objektumot
```java
// inicializálja az Outline osztály objektumot
Outline outline = new Outline();
```
## 4. lépés: Inicializálja az OutlineElement osztályobjektumot
```java
// inicializálja az OutlineElement osztály objektumot
OutlineElement outlineElem = new OutlineElement();
```
## 5. lépés: Töltse be és helyezze be a képet
```java
// tölts be egy képet
Image image = new Image(null, dataDir + "Input.jpg");
// szúrjon be képet a dokumentum csomópontjába
outlineElem.appendChildLast(image);
```
## 6. lépés: Adjon hozzá megjegyzéscímkét a képhez
```java
// adjon hozzá egy sárga csillagjegyzet címkét a képhez
NoteTag noteTag = NoteTag.createYellowStar();
image.getTags().add(noteTag);
```
## 7. lépés: Vázlatelem csomópont hozzáadása
```java
// vázlatelem csomópont hozzáadása
outline.appendChildLast(outlineElem);
```
## 8. lépés: Adjon hozzá Outline Node-t
```java
// körvonal csomópont hozzáadása
page.appendChildLast(outline);
```
## 9. lépés: Oldalcsomópont hozzáadása
```java
// oldalcsomópont hozzáadása
doc.appendChildLast(page);
```
## 10. lépés: Mentse el a OneNote-dokumentumot
```java
// mentse a OneNote-dokumentumot PDF-ként
doc.save(dataDir + "AddNewImageNodeWithTag_out.pdf", SaveFormat.Pdf);
```
Gratulálunk! Sikeresen hozzáadott egy új képcsomópontot címkével a OneNote-ban az Aspose.Note for Java használatával.
## Következtetés
 Az Aspose.Note for Java elsajátítása izgalmas lehetőségeket nyit meg a OneNote dokumentumkezelésében. Ennek az oktatóanyagnak a követésével olyan gyakorlati készségekre tett szert, amelyeket különféle projektekben lehet alkalmazni. Továbbra is tanulmányozza az Aspose.Note dokumentációját[itt](https://reference.aspose.com/note/java/) fejlettebb funkciókért és lehetőségekért.
## GYIK
### Hol találom az Aspose.Note dokumentációját?
 A dokumentációt megtalálod[itt](https://reference.aspose.com/note/java/).
### Hogyan tölthetem le az Aspose.Note for Java-t?
 Letöltheti a kiadási oldalról[itt](https://releases.aspose.com/note/java/).
### Van ingyenes próbaverzió?
 Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).
### Hol kaphatok támogatást az Aspose.Note-hoz?
 Látogassa meg a közösségi fórumot[itt](https://forum.aspose.com/c/note/28) támogatásért.
### Szükségem van ideiglenes engedélyre?
 Igény esetén ideiglenes engedélyt kaphat[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
