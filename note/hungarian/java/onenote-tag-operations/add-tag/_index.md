---
title: Címke hozzáadása a OneNote-ban – Aspose.Note
linktitle: Címke hozzáadása a OneNote-ban – Aspose.Note
second_title: Aspose.Note Java API
description: Emelje fel a OneNote-ot az Aspose.Note for Java segítségével. Könnyedén hozzáadhat címkéket lépésenkénti útmutatónk segítségével. Fokozza a szervezettséget és az együttműködést most!
weight: 12
url: /hu/java/onenote-tag-operations/add-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Címke hozzáadása a OneNote-ban – Aspose.Note

## Bevezetés
Szeretné javítani dokumentumszervezését és együttműködését a OneNote-ban Java használatával? Az Aspose.Note for Java hatékony megoldást kínál a címkék zökkenőmentes hozzáadására, biztosítva, hogy a jegyzetei ne csak informatívak, hanem vizuálisan is vonzóak legyenek. Ebben az oktatóanyagban lépésről lépésre végigvezetjük a folyamaton, hogy kiaknázhassa az Aspose.Note for Java teljes potenciálját.
## Előfeltételek
Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik az alábbiakkal:
- Java Development Kit (JDK) telepítve a rendszerére.
-  Aspose.Note a Java könyvtárhoz letöltve. Megkaphatod[itt](https://releases.aspose.com/note/java/).
- Alapvető ismeretek a Java programozásról.
## Csomagok importálása
Győződjön meg róla, hogy importálja a szükséges csomagokat a projekt elindításához:
```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.NoteTag;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TagIcon;
import com.aspose.note.ParagraphStyle;
```
Bontsuk le a fenti kódot egy lépésről lépésre útmutatóra.
## 1. lépés: Állítsa be a dokumentumot és az oldalt
Kezdje egy új dokumentum objektum létrehozásával és egy oldal objektum inicializálásával:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```
Itt beállítjuk a dokumentumok könyvtárának elérési útját, létrehozunk egy új dokumentumot, és inicializálunk egy oldalt.
## 2. lépés: Készítsen vázlatot
Ezután hozzon létre egy Outline objektumot a tartalom felépítéséhez:
```java
Outline outline = new Outline();
```
A körvonalak hierarchikus szerkezetet biztosítanak a dokumentumnak, megkönnyítve az információk rendszerezését.
## 3. lépés: Inicializálja az OutlineElement elemet és a bekezdésstílust
Most inicializáljon egy OutlineElement elemet, és állítsa be a bekezdésstílust a szöveg formázásához:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
Az OutlineElement egy elemet jelöl a vázlaton belül, a bekezdésstílus pedig a szöveg formázási tulajdonságait határozza meg.
## 4. lépés: RichText hozzáadása NoteTag-gel
Hozzon létre egy RichText objektumot, fűzze hozzá a OneNote szövegét, és adjon hozzá egy NoteTag-et:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
A RichText lehetővé teszi formázott szöveg beépítését, a NoteTag pedig vizuális jelzéseket ad a tartalomhoz.
## 5. lépés: Készítse el a vázlatos szerkezetet
Adja hozzá a szövegcsomópontot, a vázlatelem csomópontot és a vázlatcsomópontot a dokumentum szerkezetének felépítéséhez:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Ez a lépés biztosítja, hogy a tartalom rendszerezve legyen a dokumentumban.
## 6. lépés: Mentse el a dokumentumot
Mentse el a dokumentumot PDF formátumban:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Mostantól a hozzáadott címkékkel ellátott OneNote-dokumentum PDF-ként kerül mentésre.
Az alábbi lépések követésével könnyedén javíthatja OneNote-dokumentumait az Aspose.Note for Java segítségével.
## Következtetés
Ebben az oktatóanyagban megvizsgáltuk, hogyan használhatja az Aspose.Note for Java alkalmazást címkék hozzáadásához a OneNote-dokumentumokhoz. A Java programozás erejét kihasználva javíthatja jegyzetelési élményét, és tetszetős tartalmat hozhat létre.
## GYIK
### 1. Használhatom az Aspose.Note for Java programot más programozási nyelvekkel?
Az Aspose.Note elsősorban a Java-t támogatja, de vannak .NET-hez is elérhető verziók.
### 2. Alkalmas-e az Aspose.Note for Java kezdőknek?
Igen, az Aspose.Note for Java átfogó dokumentációt és támogatást nyújt, így kezdők és tapasztalt fejlesztők számára egyaránt elérhető.
### 3. Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java számára?
 Kaphat ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).
### 4. Hol találok további támogatást?
 Bármilyen kérdéssel vagy segítséggel kapcsolatban keresse fel a[Aspose.Note fórum](https://forum.aspose.com/c/note/28).
### 5. Van-e ingyenes próbaverzió?
 Igen, felfedezheti az ingyenes próbaverziót[itt](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
