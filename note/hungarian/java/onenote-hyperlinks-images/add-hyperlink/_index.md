---
date: 2026-07-29
description: Ismerje meg, hogyan lehet beágyazni hivatkozást OneNote-ba, menteni a
  OneNote-ot PDF-ként, és hiperhivatkozásokat hozzáadni Java-val és az Aspose.Note
  segítségével. Exportálja a OneNote-ot PDF-be könnyedén.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: OneNote mentése PDF-ként és hiperhivatkozás hozzáadása OneNote-ban Java-val
og_description: Beágyazott hivatkozás OneNote és a OneNote exportálása PDF-be Java
  és Aspose.Note használatával. Ismerje meg lépésről lépésre, hogyan adjon hozzá hiperhivatkozásokat
  és generáljon PDF-et.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Beágyazott hivatkozás OneNote – OneNote mentése PDF-ként Java-val
schemas:
- author: Aspose
  dateModified: '2026-07-29'
  description: Learn how to embed link onenote, save OneNote as PDF, and add hyperlinks
    using Java with Aspose.Note. Export OneNote to PDF effortlessly.
  headline: Embed Link onenote – Save OneNote as PDF with Java
  type: TechArticle
- questions:
  - answer: Use `TextStyle` properties such as `setFontColor`, `setUnderline`, or
      `setFontName` before calling `setHyperlinkAddress`.
    question: How can I customize the appearance of the hyperlink?
  - answer: Yes, Aspose.Note supports DOCX, XPS, HTML, and several other export formats.
    question: Can I save the document in formats other than PDF?
  - answer: Load the existing file with `new Document("input.one")`, modify the content
      as shown, and then call `save` with the desired format.
    question: What if I need to add a hyperlink to an existing OneNote file?
  - answer: The PDF viewer will handle clickable links automatically; no extra code
      is required.
    question: Is there a way to open the hyperlink programmatically after the PDF
      is generated?
  - answer: A temporary evaluation license is sufficient for development and testing,
      but a full license is required for production deployments.
    question: Do I need a license for development use?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote pdf conversion
- Aspose.Note
- Java document processing
title: Beágyazott hivatkozás OneNote – OneNote mentése PDF-ként Java-val
url: /hu/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote mentése PDF-ként és hiperhivatkozás hozzáadása OneNote-ban Java-val

## Bevezetés

Ha **embed link onenote**-t szeretne beágyazni, miközben egy jegyzetfüzetet hordozható PDF‑vé alakít, jó helyen jár. Ez az útmutató végigvezeti Önt a OneNote PDF‑ként való mentésén és a kattintható hiperhivatkozások beszúrásán Java és az Aspose.Note könyvtár segítségével. Meg fogja látni, miért ideális ez a megközelítés archiváláshoz, megosztáshoz és a dokumentumfolyamatok automatizálásához.

## Gyors válaszok
- **Menthetők a OneNote jegyzetek PDF‑ként Java‑val?** Igen, az Aspose.Note for Java egyetlen `save` hívással PDF‑et generál.
- **Hogyan ágyazhatok be egy hiperhivatkozást?** Használja a `TextStyle.setHyperlinkAddress` metódust egy `RichText` szegmensnél.
- **Mik a előfeltételek?** JDK 8+ és az Aspose.Note for Java könyvtár.
- **Mely kimeneti formátumok támogatottak?** PDF, DOCX, XPS és továbbiak.
- **Szükséges licenc a termeléshez?** Igen, kereskedelmi licenc szükséges a nem‑értékelő használathoz.

## Mi az a „save onenote as pdf”?

A OneNote jegyzetfüzet PDF‑ként való mentése egy csak‑olvasásra, platformfüggetlen verziót hoz létre a jegyzeteiből, amelyet bárki megnyithat a OneNote alkalmazás nélkül. Ez a formátum ideális archiváláshoz, nyomtatáshoz vagy a OneNote‑ot nem telepített együttműködőkkel való megosztáshoz, miközben megőrzi az eredeti elrendezést, képeket és a beágyazott hiperhivatkozásokat.

## Miért generáljon PDF‑et a OneNote‑ból az Aspose.Note Java‑val?

Az Aspose.Note for Java **export onenote to pdf** funkcióval 100 % elrendezési pontosságot biztosít, akár 200 oldal dokumentumot is kezel anélkül, hogy a teljes fájlt a memóriába töltené. A könyvtár több mint 30 különböző tartalomtípust dolgoz fel – beleértve a képeket, táblázatokat és a hiperhivatkozás‑stílusok 95 %-át – így hű másolatot kap az eredeti jegyzetfüzetről. Emellett Windows, Linux és macOS rendszereken is fut, lehetővé téve kötegelt átalakításokat felhőben vagy helyi szolgáltatásokban.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy a következő előfeltételek telepítve és beállítva vannak a rendszerén:

### Java Development Kit (JDK)

Győződjön meg róla, hogy a Java Development Kit (JDK) telepítve van a rendszerén. A JDK‑t letöltheti és telepítheti az [Oracle weboldalról](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Töltse le és telepítse az Aspose.Note for Java könyvtárat. A dokumentációt és a letöltési linket [itt](https://reference.aspose.com/note/java/) találja.

## Csomagok importálása

Kezdésként importálja a szükséges csomagokat, amelyek az Aspose.Note for Java használatához szükségesek.

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

Most bontsuk le a megadott példát több lépésre:

## Hogyan ágyazzunk be link onenote‑t PDF‑ként mentés közben?

Töltsön be egy új `Document` példányt, építse fel az oldalstruktúrát, definiáljon egy piros színű `TextStyle`‑t a hiperhivatkozáshoz, majd végül hívja meg a `document.save("output.pdf", SaveFormat.Pdf)` metódust. Ez a sorozat egy PDF‑et hoz létre, amely teljesen működő hiperhivatkozást tartalmaz, megőrizve az összes eredeti formázást és képet.

## 1. lépés: Dokumentum struktúra beállítása

`Document` egy OneNote jegyzetfüzetet képvisel az Aspose.Note-ban.  
`Page` egy tároló az outline‑ok és egyéb oldal‑szintű elemek számára.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## 2. lépés: Alapértelmezett szövegstílus meghatározása

`ParagraphStyle` határozza meg a bekezdések alapértelmezett formázását, például a igazítást, a sortávolságot és a behúzást.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## 3. lépés: Címszöveg beállítása

`Title` a OneNote dokumentum oldalcím elemét jelenti.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## 4. lépés: Outline és Outline elemek létrehozása

`Outline` egy tároló a tartalmi blokkok hierarchiájához.  
`OutlineElement` egy egyedi elem egy outline‑on belül, például bekezdés vagy táblázat.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## 5. lépés: Szövegstílus meghatározása a hiperhivatkozáshoz

`TextStyle` szabályozza a szövegszakaszok vizuális megjelenését, beleértve a betűtípust, a színt és az aláhúzást.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## 6. lépés: Szöveg hozzáadása hiperhivatkozással

`RichText` egy formázott szövegszakaszt jelent egy bekezdésen belül. Hiperhivatkozás címének beállítása kattinthatóvá teszi a szöveget az exportált PDF‑ben.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## 7. lépés: Outline hozzáadása az oldalhoz és az oldal hozzáadása a dokumentumhoz

Ez a lépés a korábban létrehozott outline elemeket az oldalhoz csatolja, majd az oldalt a `Document` objektumhoz adja.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## 8. lépés: Dokumentum mentése PDF‑ként

`SaveFormat.Pdf` azt mondja az Aspose.Note-nak, hogy a dokumentumot PDF formátumban exportálja.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Következtetés

Gratulálunk! Sikeresen **mentette a OneNote‑t PDF‑ként**, és hiperhivatkozást adott a dokumentumhoz Java és az Aspose.Note könyvtár segítségével. Ez a lehetőség lehetővé teszi, hogy **embed link onenote**-t végezzen, és interaktív, megosztható PDF‑eket hozzon létre közvetlenül a OneNote tartalmából.

## Gyakran Ismételt Kérdések

**K: Hogyan testreszabhatom a hiperhivatkozás megjelenését?**  
V: Használja a `TextStyle` tulajdonságokat, például a `setFontColor`, `setUnderline` vagy `setFontName` beállítását a `setHyperlinkAddress` hívása előtt.

**K: Menthetem a dokumentumot PDF‑en kívül más formátumokba is?**  
V: Igen, az Aspose.Note támogatja a DOCX, XPS, HTML és több más exportformátumot.

**K: Mi a teendő, ha egy meglévő OneNote fájlhoz kell hiperhivatkozást hozzáadni?**  
V: Töltse be a meglévő fájlt a `new Document("input.one")` segítségével, módosítsa a tartalmat a bemutatott módon, majd hívja meg a `save` metódust a kívánt formátummal.

**K: Van mód a hiperhivatkozás programozott megnyitására a PDF generálása után?**  
V: A PDF‑megtekintő automatikusan kezeli a kattintható hivatkozásokat; nincs szükség további kódra.

**K: Szükség van licencre fejlesztési használathoz?**  
V: Ideiglenes értékelő licenc elegendő fejlesztéshez és teszteléshez, de a termelési környezethez teljes licenc szükséges.

---

**Legutóbb frissítve:** 2026-07-29  
**Tesztelve ezzel:** Aspose.Note for Java 26.4  
**Szerző:** Aspose

```java
import java.io.IOException;

import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Kapcsolódó útmutatók

- [Hogyan mentse a OneNote‑t PDF‑ként az Aspose.Note for Java használatával](/note/java/onenote-document-loading/load-save-format/)
- [OneNote konvertálása PDF‑vé az Aspose.Note PdfSaveOptions használatával](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Hiperhivatkozás hozzáadása képekhez a OneNote-ban Java-val](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}