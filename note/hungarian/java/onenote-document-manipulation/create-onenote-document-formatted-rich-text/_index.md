---
date: 2026-08-18
description: Ismerje meg, hogyan menthetünk OneNote-ot PDF-ként Java-ban az Aspose.Note
  használatával, hozhatunk létre OneNote dokumentumokat, formázhatunk rich text-et,
  és exportálhatunk PDF-be. Gyors lépésről‑lépésre útmutató.
keywords:
- save onenote as pdf
- export onenote to pdf
- format rich text java
lastmod: 2026-08-18
linktitle: OneNote dokumentum létrehozása és mentése PDF-ként Java-ban
og_description: Ismerje meg, hogyan menthetünk OneNote-ot PDF-ként Java-ban az Aspose.Note
  segítségével. Ez a bemutató bemutatja a OneNote fájlok létrehozását, a rich‑text
  formázását, és a PDF-be exportálást.
og_image_alt: Screenshot of Java code converting OneNote to PDF using Aspose.Note
og_title: OneNote mentése PDF-ként Java-ban – Gyors Aspose.Note útmutató
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to save onenote as pdf in Java using Aspose.Note, create
    OneNote documents, format rich text, and export to PDF. Quick step‑by‑step guide.
  headline: How to save onenote as pdf in Java with Aspose.Note
  type: TechArticle
- description: Learn how to save onenote as pdf in Java using Aspose.Note, create
    OneNote documents, format rich text, and export to PDF. Quick step‑by‑step guide.
  name: How to save onenote as pdf in Java with Aspose.Note
  steps:
  - name: set up document and page
    text: '`Document` is Aspose.Note''s top‑level object that represents a OneNote
      file in memory. A `Page` object holds the visual elements of a OneNote page,
      such as text, images, and containers.'
  - name: create title with formatting
    text: '`ParagraphStyle` defines alignment, indentation, and spacing for a paragraph.
      `TextStyle` defines font, size, color and other character attributes for rich‑text
      runs.'
  - name: create rich text with formatting
    text: Here we build rich‑text content using several `TextStyle` objects to demonstrate
      **rich text formatting**.
  - name: add elements to page and document
    text: Combine the title and rich text into the page hierarchy so the document
      reflects the desired structure.
  - name: save document – export onenote to pdf
    text: Finally, export the OneNote document as a PDF file in one call, preserving
      all styling and layout.
  type: HowTo
- questions:
  - answer: Yes, you can adjust additional properties such as underline, strike‑through,
      and text alignment via the `TextStyle` and `ParagraphStyle` classes.
    question: Can I customize the font styles further?
  - answer: Absolutely. As long as the IDE supports standard Java development, you
      can add the Aspose.Note JAR to the project’s classpath.
    question: Is Aspose.Note for Java compatible with all Java IDEs?
  - answer: Yes, the same code works in servlet‑based or Spring Boot applications,
      enabling dynamic OneNote‑to‑PDF generation on the server side.
    question: Can I integrate this functionality into web applications?
  - answer: A commercial license is required for production use. A temporary license
      is available for evaluation and testing.
    question: Are there licensing requirements for using Aspose.Note for Java?
  - answer: It supports PDF, HTML, PNG, JPEG, and several other export formats, giving
      you flexibility to convert OneNote pages into the format you need.
    question: Does Aspose.Note for Java support other document formats besides OneNote?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- onenote
- Aspose.Note
- Java document automation
title: Hogyan menthetünk OneNote-ot PDF-ként Java-ban az Aspose.Note segítségével
url: /hu/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan mentse a OneNote-ot PDF-ként Java-ban az Aspose.Note segítségével

## Bevezetés

Ha **OneNote mentése PDF-ként** funkcióra van szüksége, miközben minden címsor, bekezdésstílus és beágyazott kép változatlan marad, jó helyen jár. Ebben a bemutatóban végigvezetjük a OneNote dokumentum létrehozását, egyedi rich‑text stílusok alkalmazását, és a közvetlen PDF‑exportálást az Aspose.Note for Java használatával. A végére egy újrahasználható kódrészletet kap, amelyet bármely Java projektbe beilleszthet a kifinomult OneNote‑PDF konverziók automatizálásához.

## Gyors válaszok
- **Mit tanít ez a bemutató?** Hogyan hozzunk létre egy OneNote dokumentumot formázott szöveggel, és mentsük PDF‑ként.  
- **Melyik könyvtár szükséges?** Aspose.Note for Java (letölthető a hivatalos oldalról).  
- **Szükségem van licencre?** Az ideiglenes licenc teszteléshez működik; a teljes licenc a termeléshez szükséges.  
- **Milyen IDE-t használhatok?** Bármely Java IDE — IntelliJ IDEA, Eclipse vagy NetBeans.  
- **Megváltoztathatom a kimeneti formátumot?** Igen, az Aspose.Note támogatja a PDF, HTML, PNG és további formátumokat.

## Mi az a “save onenote pdf”?
A OneNote PDF‑ként való mentése átalakítja a hierarchikus OneNote oldalt — szöveget, képeket, táblázatokat és formázást — egy lapos PDF dokumentummá, amely bármely eszközön megnyitható OneNote nélkül is. A konverzió megőrzi a elrendezést, betűtípusokat és beágyazott objektumokat, így hordozható, csak‑olvasásra alkalmas ábrázolást biztosít a megosztáshoz, archiváláshoz vagy nyomtatáshoz.

## Miért formázzuk a rich text-et Java-ban?
A rich text formázása Java‑ban lehetővé teszi, hogy programozottan stílusozzuk a címsorokat, bekezdéseket és beágyazott elemeket, például félkövér vagy színezett szöveget, így a generált OneNote oldalak megfelelnek a márka‑ vagy jelentési szabványoknak manuális szerkesztés nélkül. A kódban alkalmazott stílusok biztosítják a konzisztenciát, csökkentik a hibákat, és dinamikusan generálhatók dokumentumok adat vagy felhasználói bemenet alapján.

## Előkövetelmények

1. **Java Development Kit (JDK)** – bármelyik újabb verzió (8 vagy magasabb).  
2. **Aspose.Note for Java JAR** – töltsd le a [download link](https://releases.aspose.com/note/java/) oldalról.  
3. **IDE** – IntelliJ IDEA, Eclipse vagy bármely kedvelt szerkesztő.

## Csomagok importálása

Mielőtt elkezdenénk, importáljuk a szükséges osztályokat a Java fájlunkba:

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.TextStyle;
import com.aspose.note.ParagraphStyle;
import com.aspose.note.Title;
```

## Hogyan mentse a OneNote-ot PDF-ként Java-ban – lépésről‑lépésre útmutató

Töltsd be a OneNote dokumentumot, adj hozzá formázott tartalmat, és hívd meg a PDF exportálási metódust — ez a teljes munkafolyamat három tömör lépésben.

### 1. lépés: dokumentum és oldal beállítása

`Document` az Aspose.Note felső‑szintű objektuma, amely egy OneNote fájlt képvisel a memóriában.  
Egy `Page` objektum tartalmazza a OneNote oldal vizuális elemeit, például szöveget, képeket és konténereket.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

### 2. lépés: cím létrehozása formázással

`ParagraphStyle` határozza meg a bekezdés igazítását, behúzását és térközeit.  
`TextStyle` definiálja a betűtípust, méretet, színt és egyéb karakterattribútumokat a rich‑text futásokhoz.

```java
Title title = new Title();
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                        .setFontColor(Color.black)
                                        .setFontName("Arial")
                                        .setFontSize(10);

RichText titleText = new RichText().append("Title!");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
```

### 3. lépés: rich text létrehozása formázással

Itt több `TextStyle` objektumot használunk a **rich text formázás** bemutatására.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();

TextStyle textStyleForHelloWord = new TextStyle()
                                        .setFontColor(Color.red)
                                        .setFontName("Arial")
                                        .setFontSize(10);

TextStyle textStyleForOneNoteWord = new TextStyle()
                                        .setFontColor(Color.green)
                                        .setFontName("Calibri")
                                        .setFontSize(10)
                                        .setItalic(true);

TextStyle textStyleForTextWord = new TextStyle()
                                        .setFontColor(Color.blue)
                                        .setFontName("Arial")
                                        .setFontSize(15)
                                        .setBold(true)
                                        .setItalic(true);

RichText text = new RichText()
        .append("Hello", textStyleForHelloWord)
        .append(" OneNote", textStyleForOneNoteWord)
        .append(" text", textStyleForTextWord)
        .append("!", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
```

### 4. lépés: elemek hozzáadása az oldalhoz és a dokumentumhoz

A címet és a rich textet kombináljuk az oldal hierarchiájába, hogy a dokumentum a kívánt struktúrát tükrözze.

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

### 5. lépés: dokumentum mentése – OneNote exportálása PDF-be

Végül egyetlen hívással exportáljuk a OneNote dokumentumot PDF fájlba, megőrizve minden stílust és elrendezést.

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Gyakori problémák és megoldások

| Probléma | Megoldás |
|----------|----------|
| **Fájl nem található** | Ellenőrizze, hogy a `dataDir` egy létező mappára mutat, és hogy van írási jogosultsága. |
| **Hiányzó betűtípusok** | Győződjön meg róla, hogy a hivatkozott betűtípusok (pl. *Calibri*) telepítve vannak a gépen. |
| **Licenc nincs alkalmazva** | Töltse be az Aspose licencet a `Document` létrehozása előtt, hogy elkerülje a kiértékelési vízjeleket. |

## Gyakran ismételt kérdések

**K: Testreszabhatom a betűstílusokat tovább?**  
V: Igen, a `TextStyle` és `ParagraphStyle` osztályok segítségével további tulajdonságokat állíthat be, például aláhúzást, áthúzást és szövegigazítást.

**K: Az Aspose.Note for Java kompatibilis minden Java IDE‑vel?**  
V: Teljes mértékben. Amennyiben az IDE támogatja a szabványos Java fejlesztést, hozzáadhatja az Aspose.Note JAR‑t a projekt classpath‑jához.

**K: Integrálhatom ezt a funkciót webalkalmazásokba?**  
V: Igen, ugyanaz a kód működik servlet‑alapú vagy Spring Boot alkalmazásokban, lehetővé téve a dinamikus OneNote‑PDF generálást a szerveroldalon.

**K: Vannak licencelési követelmények az Aspose.Note for Java használatához?**  
V: Igen, a termelési környezetben kereskedelmi licenc szükséges. Ideiglenes licenc elérhető értékeléshez és teszteléshez.

**K: Az Aspose.Note for Java támogat más dokumentumformátumokat is a OneNote‑on kívül?**  
V: Igen, támogatja a PDF, HTML, PNG, JPEG és több exportformátumot, így rugalmasan konvertálhat OneNote oldalakat a kívánt formátumba.

## Következtetés

Ebben az útmutatóban bemutattuk, hogyan **hozzunk létre egy OneNote dokumentumot**, alkalmazzunk **rich text formázást**, és **mentsük a OneNote-ot PDF‑ként** az Aspose.Note for Java segítségével. A lépésről‑lépésre útmutató követésével automatizálhatja a kifinomult OneNote dokumentumok létrehozását és PDF‑re konvertálását bármely Java‑alapú megoldásban.

---

**Last Updated:** 2026-08-18  
**Tested With:** Aspose.Note for Java 26.5 (latest at time of writing)  
**Author:** Aspose

## Kapcsolódó bemutatók

- [Tanulja meg a OneNote PDF‑re konvertálását az Aspose.Note PdfSaveOptions használatával](/note/java/onenote-document-loading/load-pdf-save-options/)
- [OneNote PDF mentése stream‑be – Aspose.Note](/note/java/onenote-document-saving/save-onenote-document-to-stream/)
- [Speciális oldalak PDF‑ként mentése OneNote‑ban – Aspose.Note](/note/java/onenote-document-saving/specify-save-options/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}