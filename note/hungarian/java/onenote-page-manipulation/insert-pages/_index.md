---
date: 2026-08-08
description: Ismerje meg, hogyan adhat hozzá oldalakat a OneNote-hoz programozott
  módon az Aspose.Note for Java segítségével. Ez az útmutató bemutatja az oldalak
  beszúrását, az oldalstílus testreszabását, valamint a PDF vagy képfájl formátumokba
  történő exportálást.
keywords:
- add pages to onenote
- save onenote as pdf
- export onenote to png
- customize onenote page style
- convert onenote to image
lastmod: 2026-08-08
linktitle: Oldalak beszúrása a OneNote-ban – Aspose.Note
og_description: Oldalak hozzáadása a OneNote-hoz az Aspose.Note for Java segítségével.
  Ez a lépésről‑lépésre útmutató bemutatja, hogyan szúrjon be oldalakat, testreszabja
  az oldalstílust, és exportálja a jegyzetfüzetet PDF vagy PNG képek formájában.
og_image_alt: Screenshot of Java code inserting pages into a OneNote document using
  Aspose.Note
og_title: Oldalak hozzáadása a OneNote-hoz – Aspose.Note Java útmutató
schemas:
- author: Aspose
  dateModified: '2026-08-08'
  description: Learn how to add pages to OneNote programmatically using Aspose.Note
    for Java. This guide covers inserting pages, customizing page style, and exporting
    to PDF or image formats.
  headline: Add pages to OneNote - Aspose.Note
  type: TechArticle
- description: Learn how to add pages to OneNote programmatically using Aspose.Note
    for Java. This guide covers inserting pages, customizing page style, and exporting
    to PDF or image formats.
  name: Add pages to OneNote - Aspose.Note
  steps:
  - name: Java Development Kit (JDK) 8 or newer installed on your machine.
    text: Java Development Kit (JDK) 8 or newer installed on your machine.
  - name: Aspose.Note for Java library downloaded. You can download it from [Aspose.Note
      Java releases](https://releases.aspose.com/note/java/).
    text: Aspose.Note for Java library downloaded. You can download it from [Aspose.Note
      Java releases](https://releases.aspose.com/note/java/).
  - name: An IDE such as IntelliJ IDEA or Eclipse for writing and running Java code.
    text: An IDE such as IntelliJ IDEA or Eclipse for writing and running Java code.
  type: HowTo
- questions:
  - answer: Create additional `Page` objects, configure their levels and content,
      and call `document.getPages().add(page)` for each new page, just as shown in
      the examples above.
    question: How do I programmatically add more than three pages?
  - answer: Yes. Use `page.setBackgroundColor(Color.fromArgb(255, 240, 240, 240))`
      before appending the page to the document.
    question: Can I change the background color of a OneNote page?
  - answer: Load each source file into a separate `Document` instance, iterate over
      its pages, and add them to a target `Document` using the same `add` method.
    question: Is it possible to merge multiple OneNote files into one?
  - answer: Export to PNG or TIFF (`SaveFormat.Png` / `SaveFormat.Tiff`) to retain
      loss‑less quality, especially for screenshots or scanned content.
    question: What format should I use for high‑resolution images?
  - answer: Yes. Provide the password when constructing the `Document` object with
      the overload that accepts a `PasswordProvider`.
    question: Does Aspose.Note handle encrypted OneNote files?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- add pages to onenote
- Aspose.Note
- Java OneNote API
title: Oldalak hozzáadása a OneNote-hoz – Aspose.Note
url: /hu/java/onenote-page-manipulation/insert-pages/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oldalak hozzáadása a OneNote-hoz – Aspose.Note

## Bevezetés

Ezen az oktatóanyagon megtanulja, hogyan **adhat hozzá oldalakat a OneNote-hoz** programozott módon az Aspose.Note for Java használatával. A útmutató végére képes lesz új oldalakat létrehozni, egyedi stílusokat alkalmazni, és a jegyzetfüzetet PDF vagy nagy felbontású képformátumokba, például PNG-be exportálni. Ezek a képességek elengedhetetlenek, ha automatikusan kell OneNote jelentéseket generálni, tartalmakat több forrásból egyesíteni, vagy megfelelőség miatt archiv PDF-eket készíteni.

## Gyors válaszok
- **Mi a fő cél?** Új oldalak programozott hozzáadása egy OneNote dokumentumhoz.  
- **Melyik könyvtár szükséges?** Aspose.Note for Java.  
- **Menthető a kimenet PDF‑ként?** Igen – használja a `SaveFormat.Pdf`-t.  
- **Hogyan lehet képeket kapni a OneNote-ból?** Mentse a dokumentumot képformátumokkal, például BMP, PNG vagy JPEG, hogy **a OneNote-ot képpé konvertálja**.  
- **Szükség van licencre?** Érvényes Aspose.Note licenc szükséges a termelési használathoz.

## Hogyan adhatunk hozzá oldalakat a OneNote-hoz?

Töltsön be vagy hozzon létre egy `Document` objektumot, építsen egy vagy több `Page` objektumot a kívánt tartalommal, fűzze hozzá az oldalakat a dokumentumhoz, majd végül hívja meg a `save` metódust a szükséges formátummal. Ez az vég‑végi folyamat lehetővé teszi oldalak beszúrását, stílusuk alkalmazását, és az eredmény exportálását egyetlen, könnyen olvasható metódusláncban.

## Mi az oldalak hozzáadása a OneNote-hoz?

A `add pages to onenote` kifejezés az új oldalobjektumok programozott beszúrását jelenti egy meglévő OneNote jegyzetfüzetbe az Aspose.Note API használatával. A művelet teljesen memóriában zajlik, így nagy jegyzetfüzeteket is kezelhet a OneNote kliens megnyitása nélkül.

## Miért használjuk az Aspose.Note for Java-t?

Az Aspose.Note **20+ kimeneti formátumot** támogat (köztük PDF, PNG, JPEG, BMP és TIFF), és képes több száz oldalas jegyzetfüzeteket feldolgozni, miközben a memóriahasználat 150 MB alatt marad. A könyvtár bármely Java‑kompatibilis platformon fut, így platformközi rugalmasságot biztosít Microsoft Office telepítése nélkül.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg, hogy a következők rendelkezésre állnak:
1. Java Development Kit (JDK) 8 vagy újabb a gépén telepítve.  
2. Aspose.Note for Java könyvtár letöltve. Letöltheti a [Aspose.Note Java releases](https://releases.aspose.com/note/java/) oldalról.  
3. Egy IDE, például IntelliJ IDEA vagy Eclipse a Java kód írásához és futtatásához.  

## Csomagok importálása

Először importálja a szükséges osztályokat a Java forrásfájlban:

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

## 1. lépés: dokumentumobjektum létrehozása

A `Document` a felső szintű osztály, amely egy OneNote fájlt reprezentál a memóriában. Miután példányosította, az összes további művelet (oldalak hozzáadása, stílus, mentés) ezen az objektumon keresztül történik.

```java
Document doc = new Document();
```

## 2. lépés: oldalobjektumok inicializálása

A `Page` egyetlen OneNote oldalt képvisel. beállíthatja a hierarchiai szintjét, a címét és a elrendezését, mielőtt bármilyen tartalmat hozzáadna.

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## 3. lépés: csomópontok hozzáadása az oldalakhoz

A `Outline` egy tároló, amely olyan elemeket tartalmaz, mint a szöveg, képek és táblázatok egy OneNote oldalon.

```java
// Adding nodes to first Page
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

// Repeat similar steps for other pages
```

## 4. lépés: oldalak hozzáadása a dokumentumhoz

Egy `Page` objektum hozzáfűzése a `Document`‑hez a kívánt pozícióba illeszti be a jegyzetfüzet hierarchiájában.

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## 5. lépés: dokumentum mentése

A `SaveFormat` felsorolja a támogatott kimeneti formátumokat (PDF, PNG, JPEG stb.) egy OneNote dokumentum mentéséhez.

```java
String dataDir = "Your Document Directory";

doc.save(dataDir + "InsertPages_out.bmp" , SaveFormat.Bmp);
doc.save(dataDir + "InsertPages_out.pdf", SaveFormat.Pdf);
doc.save(dataDir + "InsertPages_out.gif", SaveFormat.Gif);
doc.save(dataDir + "InsertPages_out.jpeg", SaveFormat.Jpeg);
doc.save(dataDir + "InsertPages_out.png", SaveFormat.Png);
doc.save(dataDir + "InsertPages_out.tiff", SaveFormat.Tiff);

System.out.println("Files Saved Successfully!");
```

## Gyakori problémák és megoldások

- **Memóriahasználat nagyon nagy jegyzetfüzeteknél** – használja a `Document.save`‑et a `SaveOptions`‑szal, amely engedélyezi a streaminget, hogy alacsony memóriaigényt biztosítson.  
- **Hiányzó betűkészletek az exportált PDF‑ekben** – ágyazza be a szükséges betűket a `PdfSaveOptions.setEmbedFonts(true)` beállításával.  
- **A képek elmosódottak** – exportáljon PNG vagy TIFF formátumba a veszteségmentes minőségért; állítsa be a DPI‑t a `ImageSaveOptions.setResolution(300)` segítségével.

## Gyakran ismételt kérdések

**Q: Hogyan adhatok programozott módon több mint három oldalt?**  
A: Hozzon létre további `Page` objektumokat, állítsa be a szintjeiket és tartalmukat, és hívja meg a `document.getPages().add(page)` metódust minden új oldalhoz, ahogy a fenti példákban látható.

**Q: Megváltoztathatom egy OneNote oldal háttérszínét?**  
A: Igen. Használja a `page.setBackgroundColor(Color.fromArgb(255, 240, 240, 240))` metódust, mielőtt hozzáfűzné az oldalt a dokumentumhoz.

**Q: Lehetséges több OneNote fájlt egybeolvasztani?**  
A: Töltse be minden forrásfájlt egy külön `Document` példányba, iteráljon a lapjaikon, és adja hozzá őket egy cél `Document`‑hez ugyanazzal az `add` metódussal.

**Q: Milyen formátumot használjak nagy felbontású képekhez?**  
A: Exportáljon PNG vagy TIFF formátumba (`SaveFormat.Png` / `SaveFormat.Tiff`) a veszteségmentes minőség megőrzéséhez, különösen képernyőképek vagy beolvasott tartalom esetén.

**Q: Kezeli az Aspose.Note a titkosított OneNote fájlokat?**  
A: Igen. Adja meg a jelszót a `Document` objektum létrehozásakor azon túlterheléssel, amely `PasswordProvider`‑t fogad.

## További GYIK

**Q: Beszúrhatok képeket a OneNote dokumentumba az Aspose.Note for Java használatával?**  
A: Igen. Használja az `Image` osztályt egy kép fájl betöltéséhez, és adja hozzá egy oldal csomópontgyűjteményéhez.

**Q: Az Aspose.Note kompatibilis a OneNote különböző verzióival?**  
A: Az Aspose.Note működik a OneNote 2016‑tal, a Windows 10‑es OneNote‑dal és a OneNote webes formátummal, biztosítva a zökkenőmentes integrációt a verziók között.

**Q: Hogyan kezeljem a hibákat vagy kivételeket az Aspose.Note használata közben?**  
A: Tegye a kódját try‑catch blokkokba, és fogja el az `Exception` vagy a specifikusabb `AsposeNoteException` kivételeket, hogy elegánsan kezelje a fájlhozzáférési hibákat vagy a nem támogatott tartalmakat.

**Q: Támogatja az Aspose.Note a platformközi fejlesztést?**  
A: Teljes mértékben. A könyvtár Windows, Linux és macOS rendszereken fut, amennyiben kompatibilis JDK áll rendelkezésre.

**Q: Testreszabhatom a beszúrt oldalak megjelenését a OneNote‑ban?**  
A: Igen. Beállíthatja az oldal margóit, háttérszíneit, alapértelmezett betűtípusait, és akár egyedi, CSS‑szerű stílusokat is alkalmazhat az API‑n keresztül.

---

**Legutóbb frissítve:** 2026-08-08  
**Tesztelve ezzel:** Aspose.Note for Java 24.11  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó oktatóanyagok

- [Oldalcím beállítása a Microsoft OneNote stílusában – Aspose.Note](/note/java/onenote-text-manipulation/setting-page-title-in-microsoft-onenote-style/)
- [Aspose Java oktatóanyag – Információk lekérése a OneNote oldalakról – Aspose.Note](/note/java/onenote-page-manipulation/get-information-about-pages/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}