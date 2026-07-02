---
date: 2026-01-28
description: Ismerje meg, hogyan hozhat létre vázlatot a OneNote-ban, hogyan adhat
  hozzá címkét a OneNote-hoz, és hogyan generálhat PDF-et a OneNote-ból az Aspose.Note
  for Java segítségével.
linktitle: Create Outline in OneNote and Add Tag – Aspose.Note
second_title: Aspose.Note Java API
title: Vázlat létrehozása a OneNote-ban és címke hozzáadása – Aspose.Note
url: /hu/java/onenote-tag-operations/add-tag/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vázlat létrehozása a OneNote-ban és címke hozzáadása – Aspose.Note

## Bevezetés
Szeretne **vázlatot létrehozni a OneNote-ban** és a címkék segítségével fokozni az együttműködést Java-val? Az Aspose.Note for Java egyszerűvé teszi a címkék hozzáadását, a jegyzetek struktúrájának kialakítását, és még **PDF generálását a OneNote** fájlokból is. Ebben az útmutatóban lépésről lépésre bemutatjuk, elmagyarázzuk, *miért* fontos minden rész, és megmutatjuk, hogyan készíthetünk egy kifinomult PDF-et a végén.

## Gyors válaszok
- **Mit jelent a “create outline in OneNote”?** Egy hierarchikus struktúrát (vázlatokat) épít, amely a tartalmat, például a címsorokat és alfejezeteket szervezi.
- **Melyik könyvtár ad hozzá címkéket a OneNote-hoz?** Az Aspose.Note for Java biztosítja a `NoteTag` osztályt a vizuális jelölőkhöz.
- **Exportálhatom az eredményt PDF-be?** Igen – használja a `SaveFormat.Pdf`-t a **PDF generálásához a OneNote**-ból.
- **Szükségem van licencre a termeléshez?** Ideiglenes licenc elérhető teszteléshez; teljes licenc szükséges kereskedelmi felhasználáshoz.
- **Mik a fő előfeltételek?** Telepített JDK, az Aspose.Note for Java könyvtár, és alapvető Java ismeretek.

## Mi az a “create outline in OneNote”?
A vázlat létrehozása a OneNote-ban azt jelenti, hogy `Outline` és `OutlineElement` objektumokat adunk hozzá, amelyek fastruktúrát definiálnak a jegyzetekhez. Ez a hierarchia lehetővé teszi az információk összecsukását, kibontását és szervezését, akárcsak a dokumentumok címsorai.

## Miért adjunk címkét a OneNote-hoz?
A csillagok, jelölőnégyzetek vagy egyedi ikonokhoz hasonló címkék vizuális jelzéseket adnak az olvasóknak, javítják a kereshetőséget, és segítik a csapatokat az elemek priorizálásában. Az Aspose.Note segítségével programozottan csatolhat egy `NoteTag`-et bármely szövegrészhez.

## Előfeltételek
- Java Development Kit (JDK) telepítve.
- Aspose.Note for Java könyvtár letöltve. Letöltheti [itt](https://releases.aspose.com/note/java/).
- Alapvető Java programozási ismeretek.

## Csomagok importálása
Ensure you import the necessary packages to kickstart your project:
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
Törjük le a fenti kódot egy lépésről‑lépésre útmutatóra.

## 1. lépés: Dokumentum és oldal beállítása
Kezdje egy új `Document` objektum létrehozásával és egy `Page` objektum inicializálásával:
```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## 2. lépés: Vázlat létrehozása
Ezután hozzon létre egy `Outline` objektumot a tartalom struktúrájához:
```java
Outline outline = new Outline();
```
Az outline-ok hierarchikus struktúrát biztosítanak a dokumentumhoz, megkönnyítve a **vázlat létrehozását a OneNote-ban** és az információk rendezését.

## 3. lépés: OutlineElement és ParagraphStyle inicializálása
Most inicializáljon egy `OutlineElement`-et és állítsa be a `ParagraphStyle`-t a szövegformázáshoz:
```java
OutlineElement outlineElem = new OutlineElement();
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.black)
                                .setFontName("Arial")
                                .setFontSize(10);
```
`OutlineElement` egy elemet képvisel a vázlatban, a `ParagraphStyle` pedig a szövegformázási tulajdonságokat határozza meg.

## 4. lépés: RichText hozzáadása NoteTag-gel
Hozzon létre egy `RichText` objektumot, fűzze hozzá a OneNote szövegét, és adjon hozzá egy `NoteTag`-et:
```java
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```
`RichText` lehetővé teszi a formázott szöveg beillesztését, a `NoteTag` pedig **címkét ad a OneNote-hoz** vizuális jelzésként.

## 5. lépés: Vázlat struktúra felépítése
Adja hozzá a szövegcserjét, az outline element csomópontot és az outline csomópontot a dokumentum struktúrájának felépítéséhez:
```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```
Ez a lépés biztosítja, hogy a tartalom a dokumentumban rendezett legyen, befejezve a **vázlat létrehozását a OneNote-ban** folyamatot.

## 6. lépés: Dokumentum mentése
Mentse a dokumentumot PDF formátumban, amely **PDF-et generál a OneNote-ból**:
```java
doc.save(dataDir + "AddTag_out.pdf", SaveFormat.Pdf);
System.out.printf("File Saved: %s\n", dataDir + "AddTag_out.pdf");
```
Most a hozzáadott címkékkel ellátott OneNote dokumentuma PDF-ként van mentve.

Ezeket a lépéseket követve könnyedén fejlesztheti OneNote dokumentumait az Aspose.Note for Java segítségével.

## Következtetés
Ebben az útmutatóban azt vizsgáltuk, hogyan **hozzunk létre vázlatot a OneNote-ban**, hogyan adjunk címkét a OneNote-hoz, majd hogyan **generáljunk PDF-et a OneNote-ból** az Aspose.Note for Java használatával. A Java kihasználása teljes kontrollt biztosít a jegyzetstruktúra, a vizuális címkézés és az exportálási lehetőségek felett, így jegyzetei rendezettebbek és megoszthatóbbak lesznek.

## Gyakran ismételt kérdések
### 1. Használhatom az Aspose.Note for Java-t más programozási nyelvekkel?
Az Aspose.Note elsősorban Java-t támogat, de elérhetők verziók .NET-hez is.

### 2. Alkalmas-e az Aspose.Note for Java kezdőknek?
Igen, az Aspose.Note for Java átfogó dokumentációt és támogatást nyújt, így kezdők és tapasztalt fejlesztők számára egyaránt hozzáférhető.

### 3. Hogyan szerezhetek ideiglenes licencet az Aspose.Note for Java-hoz?
Az ideiglenes licencet [itt](https://purchase.aspose.com/temporary-license/) szerezheti meg.

### 4. Hol találok további támogatást?
Bármilyen kérdés vagy segítség esetén látogassa meg az [Aspose.Note fórumot](https://forum.aspose.com/c/note/28).

### 5. Elérhető ingyenes próba?
Igen, egy ingyenes próbát [itt](https://releases.aspose.com/) tekinthet meg.

**Additional Q&A**

**K: Testreszabhatom a címke ikont?**  
V: Igen – az Aspose.Note számos előre definiált ikont biztosít a `TagIcon` segítségével, és lehetővé teszi egyedi képek használatát.

**K: Hogyan változtathatom meg a PDF kimeneti beállításokat?**  
V: Használja a `PdfSaveOptions`-t a képminőség, tömörítés és biztonság szabályozásához, mielőtt meghívná a `doc.save`-t.

**K: Lehetséges több címkét hozzáadni ugyanahhoz a szöveghez?**  
V: Teljesen lehetséges. Hívja meg a `text.getTags().add()`-t többször különböző `NoteTag` példányokkal.

---

**Last Updated:** 2026-01-28  
**Tested With:** Aspose.Note for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}