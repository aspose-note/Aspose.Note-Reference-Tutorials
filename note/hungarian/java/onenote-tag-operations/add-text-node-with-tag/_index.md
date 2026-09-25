---
date: 2026-09-24
description: Ismerje meg, hogyan adhat hozzá címkét egy OneNote dokumentumhoz az Aspose.Note
  for Java segítségével – hozzon létre egy OneNote fájlt, adjon hozzá egy stílusos
  szöveges csomópontot címkével, és mentse csak néhány kódsorral.
keywords:
- how to add tag
- Aspose.Note Java
- OneNote tag operations
- add text node
lastmod: 2026-09-24
linktitle: Szöveges csomópont hozzáadása címkével a OneNote-ban – Aspose.Note
og_description: Ismerje meg, hogyan adhat hozzá címkét egy OneNote dokumentumhoz az
  Aspose.Note for Java segítségével – hozzon létre egy OneNote fájlt, adjon hozzá
  egy stílusos szöveges csomópontot címkével, és mentse csak néhány kódsorral.
og_image_alt: Guide showing how to add a tag to a OneNote document using Aspose.Note
  for Java
og_title: Hogyan adjon hozzá címkét egy OneNote dokumentumhoz az Aspose.Note (Java)
  segítségével
schemas:
- author: Aspose
  dateModified: '2026-09-24'
  description: Learn how to add tag to a OneNote document with Aspose.Note for Java
    – create a OneNote file, add a styled text node with a tag, and save it in just
    a few lines of code.
  headline: How to add tag to a OneNote document by adding a text node using Aspose.Note
  type: TechArticle
- questions:
  - answer: It provides a Java API to read, modify, and create OneNote files without
      needing Microsoft Office installed.
    question: What does Aspose.Note do?
  - answer: Roughly 15 lines, including object creation and styling.
    question: How many lines of code to add a tagged text node?
  - answer: A free trial works for development; a license is required for production
      use.
    question: Do I need a license to run the sample?
  - answer: Yes – Aspose.Note offers over 30 built‑in icons such as yellow star, checkmark,
      and heart.
    question: Can I change the tag icon?
  - answer: The library saves the result as a standard *.one* OneNote file.
    question: What format is the output file?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- OneNote
- Aspose.Note
- Java
- tag operations
- document creation
title: Hogyan adjon hozzá címkét egy OneNote dokumentumhoz szöveges csomópont hozzáadásával
  az Aspose.Note segítségével
url: /hu/java/onenote-tag-operations/add-text-node-with-tag/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjon hozzá címkét egy OneNote dokumentumhoz szövegcsomópont hozzáadásával az Aspose.Note használatával

## Bevezetés
Ebben az útmutatóban megtanulja, **hogyan adjon hozzá címkét** egy OneNote dokumentumhoz az Aspose.Note Java API használatával. Lépésről lépésre végigvezetjük egy új OneNote fájl létrehozását, egy bekezdés formázását, egy beépített címke csatolását a szöveghez, és végül a jegyzetfüzet mentését egyetlen `save` hívással. Akár személyes jegyzetkészítő eszközt épít, akár vállalati jelentéskészítést automatizál, az alábbi lépések teljes programozási irányítást biztosítanak a OneNote tartalom felett.

## Gyors válaszok
- **Mi a feladata az Aspose.Note-nak?** Egy Java API-t biztosít OneNote fájlok olvasásához, módosításához és létrehozásához anélkül, hogy a Microsoft Office telepítve lenne.  
- **Hány kódsor szükséges egy címkézett szövegcsomópont hozzáadásához?** Körülbelül 15 sor, beleértve az objektumok létrehozását és a formázást.  
- **Szükségem van licencre a példa futtatásához?** Egy ingyenes próba verzió fejlesztéshez megfelelő; licenc szükséges a termeléshez.  
- **Módosíthatom a címke ikont?** Igen – az Aspose.Note több mint 30 beépített ikont kínál, például sárga csillag, pipa és szív.  
- **Mi a kimeneti fájl formátuma?** A könyvtár a eredményt egy szabványos *.one* OneNote fájlként menti.

## Mit jelent a „OneNote dokumentum létrehozása”?
A OneNote dokumentum létrehozása azt jelenti, hogy programozott módon generálunk egy *.one* fájlt, amely megnyitható a Microsoft OneNote-ban. A fájl oldalakat, vázlatokat és gazdag szöveges elemeket tartalmaz, amelyeket az Aspose.Note API-val építenek, lehetővé téve a jegyzetfüzetek létrehozását asztali alkalmazás vagy egyéb nélkül.

## Miért adjon hozzá egy szövegcsomópontot címkével?
A címke hozzáadása egy szövegcsomóponthoz kiemeli a fontos információkat, és lehetővé teszi a OneNote beépített címke-navigációját, amely felgyorsítja az átnézést és a feladatkezelést. A címkék metaadatként tárolódnak, így eszközök között megmaradnak és megtartják vizuális ikonjaikat. Ez továbbá lehetővé teszi a felhasználók számára, hogy hatékonyan szűrjék vagy keressék a címkézett elemeket nagy jegyzetfüzetekben.

## Előfeltételek
Mielőtt belemerülnénk az útmutatóba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
- Alapvető Java programozási ismeretek.  
- Aspose.Note for Java könyvtár telepítve. Letöltheti az Aspose.Note for Java könyvtárat [letöltés Aspose.Note for Java](https://releases.aspose.com/note/java/).  
- Egy Java fejlesztéshez beállított integrált fejlesztői környezet (IDE).

## Csomagok importálása
Kezdje a szükséges csomagok importálásával a Java projektjéhez. A kódban tartalmazza a következő importálásokat:
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

## 1. lépés: dokumentum objektum létrehozása
`Document` a felső szintű osztály, amely egy OneNote fájlt reprezentál a memóriában. Az példányosítás után minden további művelet ezen az objektumon keresztül folyik.
```java
// The path to the documents directory.
String dataDir = "Your Document Directory";
// Create an object of the Document class
Document doc = new Document();
```

## 2. lépés: oldal osztály objektum inicializálása
`Page` egyetlen oldalt képvisel a OneNote jegyzetfüzetben. Minden oldal több vázlatot és egyéb elemet is tartalmazhat.
```java
// Initialize Page class object
Page page = new Page();
```

## 3. lépés: outline osztály objektum inicializálása
`Outline` a kapcsolódó elemeket csoportosítja az oldalon, és egy vagy több `OutlineElement` objektum tárolójaként működik.
```java
// Initialize Outline class object
Outline outline = new Outline();
```

## 4. lépés: outlineelement osztály objektum inicializálása
`OutlineElement` a legkisebb vizuális egység, amely szöveget, képeket vagy egyéb gazdag tartalmat tartalmazhat egy vázlaton belül.
```java
// Initialize OutlineElement class object
OutlineElement outlineElem = new OutlineElement();
```

## 5. lépés: szövegstílus testreszabása
Állítsa be a szövegcsomópont stílusát – itt **állítja be a bekezdés stílusát**, például a betűszínt, nevét és méretét. Az Aspose.Note lehetővé teszi RGB színek, betűcsaládok és pontméretek megadását egyetlen `RichTextStyle` objektumban.
```java
// Customize text style
ParagraphStyle textStyle = new ParagraphStyle()
                                .setFontColor(Color.BLACK)
                                .setFontName("Arial")
                                .setFontSize(10);
```

## 6. lépés: richtext objektum létrehozása
`RichText` az az osztály, amely a tényleges karakterlánc tartalmat tárolja. Az objektum létrehozása után hozzáfűzi a kívánt szöveget, amely később megkapja a címkét.
```java
// Create RichText object
RichText text = new RichText().append("OneNote text.");
text.setParagraphStyle(textStyle);
```

## 7. lépés: jegycímke hozzáadása
`Tag` egy vizuális jelölőt (pl. sárga csillag) képvisel, amely bármely `RichText`-hez csatolható. Az Aspose.Note több mint 30 beépített címke ikont kínál, és szükség esetén egyedi ikonok is definiálhatók.
```java
// Add note tag
NoteTag noteTag = NoteTag.createYellowStar();
text.getTags().add(noteTag);
```

## 8. lépés: szövegcsomópont hozzáadása
Csatolja a `RichText`-et (címkéjével együtt) a `OutlineElement`-hez. Ez a lépés a formázott, címkézett szöveget a vázlat hierarchiához köti.
```java
// Add text node
outlineElem.appendChildLast(text);
```

## 9. lépés: outline elem hozzáadása az outline-hoz
Helyezze a `OutlineElement`-et az `Outline` tárolóba, hogy az az oldal vizuális struktúrájának része legyen.
```java
// Add outline element node
outline.appendChildLast(outlineElem);
```

## 10. lépés: outline hozzáadása az oldalhoz
Illessze be az `Outline`-t a `Page` struktúrába, befejezve az oldal tartalomfáját.
```java
// Add outline node
page.appendChildLast(outline);
```

## 11. lépés: oldal hozzáadása a dokumentumhoz
Adja hozzá a teljesen felépített `Page`-t a `Document` objektumhoz, előkészítve a jegyzetfüzetet a mentéshez.
```java
// Add page node
doc.appendChildLast(page);
```

## 12. lépés: OneNote dokumentum mentése
Végül **mentse a OneNote fájlt** a lemezre. Ez befejezi a **OneNote dokumentum létrehozása** munkafolyamatot, és egy szabványos *.one* fájlt hoz létre, amely bármely újabb Microsoft OneNote verzióval megnyitható.
```java
// Save OneNote document
doc.save(dataDir + "AddTextNodeWithTag_out.one");
```

## Miért fontos ez
Az Aspose.Note **50+ bemeneti és kimeneti formátumot** támogat (beleértve a DOCX, PDF, HTML és képtípusokat), és képes több száz oldalas jegyzetfüzeteket feldolgozni anélkül, hogy a teljes fájlt a memóriába töltené, így alkalmas szerveroldali automatizálásra és nagyszabású jegyzetgenerálásra.

## Gyakori problémák és megoldások
- **A címke nem jelenik meg a mentés után** – Győződjön meg arról, hogy a `richText.getTags().add(tag)` hívást a `RichText` `OutlineElement`-hez való csatolása előtt hajtja végre.  
- **A betűstílus figyelmen kívül marad** – Ellenőrizze, hogy a `RichTextStyle` a `RichText` példányra van alkalmazva, mielőtt hozzáadná a vázlathoz.  
- **Nagy jegyzetfüzetek OutOfMemoryError-t okoznak** – Használja a `Document.setLoadOptions(new LoadOptions(LoadFormat.ONE))` hívást a streaming mód engedélyezéséhez 500 MB-nál nagyobb fájlok esetén.

## Gyakran ismételt kérdések
### K: Használhatom az Aspose.Note for Java-t más Java könyvtárakkal?
I: Igen, az Aspose.Note for Java zökkenőmentesen integrálódik olyan könyvtárakkal, mint az Apache POI, Jackson vagy Spring, lehetővé téve a jegyzetkészítés kombinálását adatfeldolgozó csővezetékekkel.

### K: Elérhető ingyenes próba verzió az Aspose.Note for Java-hoz?
I: Igen, hozzáférhet az ingyenes próba verzióhoz az Aspose.Note ingyenes próba oldalán [letöltés Aspose.Note free trial page](https://releases.aspose.com/).

### K: Hogyan kaphatok támogatást az Aspose.Note for Java-hoz?
I: Támogatást kérhet az Aspose.Note közösségtől az Aspose.Note fórumon [Aspose.Note forum](https://forum.aspose.com/c/note/28).

### K: Elérhetők ideiglenes licencek az Aspose.Note for Java-hoz?
I: Igen, ideiglenes licenceket szerezhet a [temporary license purchase page](https://purchase.aspose.com/temporary-license/) oldalon.

### K: Hol találom az Aspose.Note for Java dokumentációját?
I: A dokumentáció elérhető az Aspose.Note Java API dokumentációban [Aspose.Note Java API documentation](https://reference.aspose.com/note/java/).

---

**Utolsó frissítés:** 2026-09-24  
**Tesztelt verzió:** Aspose.Note for Java 24.11  
**Szerző:** Aspose

## Kapcsolódó útmutatók

- [Címkék hozzáadása a OneNote-hoz – Címkézett OneNote dokumentum létrehozása az Aspose.Note használatával](/note/java/onenote-tag-operations/)
- [Találkozó jegyzet sablon generálása az Aspose.Note for Java-val – Vázlat létrehozása a OneNote-ban](/note/java/onenote-tag-operations/generate-template-for-meeting-notes/)
- [OneNote dokumentum létrehozása Java – Aspose Note Java útmutató](/note/java/onenote-document-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}