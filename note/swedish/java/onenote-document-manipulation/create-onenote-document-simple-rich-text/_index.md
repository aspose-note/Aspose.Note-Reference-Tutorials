---
date: 2026-08-18
description: Lär dig hur du exporterar OneNote till PDF, ställer in styckeformatering
  i Java och sparar OneNote som PDF med Aspose.Note för Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Ställ in styckeformat när du skapar OneNote-dokument i Java
og_description: Exportera OneNote till PDF och ställ in styckeformat i Java med Aspose.Note.
  Följ den här steg-för-steg-guiden för att enkelt skapa professionella PDF-filer.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Exportera OneNote till PDF med styckeformat i Java (58 tecken)
schemas:
- author: Aspose
  dateModified: '2026-08-18'
  description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  headline: How to export OneNote to PDF with paragraph style in Java
  type: TechArticle
- description: Learn how to export OneNote to PDF, set paragraph formatting in Java,
    and save OneNote as PDF using Aspose.Note for Java.
  name: How to export OneNote to PDF with paragraph style in Java
  steps:
  - name: set document directory
    text: Define where the generated files will be saved. Replace `"Your Document
      Directory"` with an absolute or relative path on your machine.
  - name: initialize document object
    text: Create the root `Document` that represents the OneNote file. **Definition
      anchor:** `Document` is Aspose.Note’s top‑level object that holds one or more
      pages in memory.
  - name: initialize page object
    text: A OneNote file consists of one or more pages; we start with a single page.
      **Definition anchor:** `Page` represents a single OneNote page, containing outlines,
      images, and other elements.
  - name: initialize outline object
    text: Outlines act as containers for outline elements (think of them as sections).
      **Definition anchor:** `Outline` groups related `OutlineElement` objects and
      defines their visual hierarchy.
  - name: initialize outline element object
    text: Here we **add outline element** that will hold our rich text. **Definition
      anchor:** `OutlineElement` is a leaf node inside an `Outline` that can contain
      text, images, or other media.
  - name: set text style (set paragraph style)
    text: '`ParagraphStyle` defines the font family, size, color, and other typographic
      attributes for a paragraph. The `ParagraphStyle` instance defines the font,
      size, and color—this is where we **set paragraph style** for the upcoming text
      node.'
  - name: initialize rich text object
    text: '`RichText` is the node that stores styled text within an `OutlineElement`.
      We create a `RichText` node, insert a simple string, and attach the previously
      defined style.'
  - name: add rich text node to outline element
    text: Now the styled text lives inside the outline element.
  - name: add outline element node to outline
    text: The outline now contains the element that holds our paragraph.
  - name: add outline node to page
    text: We place the outline onto the page.
  type: HowTo
- questions:
  - answer: Yes, the API supports tables, images, hyperlinks, and advanced layout
      features in addition to plain text.
    question: Can Aspose.Note handle complex formatting such as tables or images?
  - answer: Direct conversion isn’t provided, but you can extract PDF content and
      rebuild a OneNote document using the API.
    question: Is it possible to convert a OneNote PDF back to a OneNote file?
  - answer: Absolutely. Aspose.Note for Java is platform‑independent; just ensure
      a compatible JDK is installed.
    question: Does the library work on Linux/macOS environments?
  - answer: Create additional `Page` and `Outline` objects, then append them to the
      `Document` just like the single‑page example.
    question: How do I add multiple pages or outlines?
  - answer: The official Aspose.Note documentation and the [support forum](https://forum.aspose.com/c/note/28)
      contain many code samples and real‑world scenarios.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- export onenote
- aspose.note
- java document processing
title: Hur man exporterar OneNote till PDF med styckeformat i Java
url: /sv/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in styckeformat medan du skapar OneNote-dokument i Java

## Introduktion

Att programatiskt exportera OneNote till PDF är ett vanligt krav för rapporteringsmotorer, automatiserade anteckningstjänster och dokumentkonverteringspipelines. I den här handledningen kommer du att lära dig hur man **export OneNote to PDF**, tillämpar anpassad styckeformatering och sparar OneNote-filen – allt med Aspose.Note för Java. I slutet har du ett färdigt Java‑exempel som producerar en polerad PDF med exakt det utseende du definierat.

## Snabba svar
- **Vad betyder “set paragraph style”?** Det tillämpar teckensnitt, storlek, färg och andra formateringsattribut på ett textstycke.  
- **Kan jag exportera resultatet till PDF?** Ja – handledningen avslutas med att spara OneNote-filen som en PDF.  
- **Behöver jag en licens för Aspose.Note?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktionsanvändning.  
- **Vilka IDE:er stöds?** Alla Java‑IDE:er – Eclipse, IntelliJ IDEA, NetBeans osv.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grunddokument.

## Hur exporterar man OneNote till PDF i Java?

`Document` representerar en OneNote‑fil som innehåller sidor, konturer och andra element. Ladda ditt OneNote‑dokument med `new Document()` (eller skapa ett nytt) och anropa `document.save("output.pdf", SaveFormat.Pdf)`. Aspose.Note skriver PDF‑filen i ett enda pass, bevarar stilar, bilder och konturer utan att Microsoft OneNote behöver vara installerat. Detta direkta tillvägagångssätt fungerar på Windows, Linux och macOS med vilken JDK 1.8+ som helst.

## Vad är “set paragraph style” i Aspose.Note?

`ParagraphStyle` är klassen som lagrar teckensnittsnamn, storlek, färg, justering och andra typografiska inställningar för ett stycke. Genom att fästa en `ParagraphStyle`‑instans på en `RichText`‑nod styr du exakt hur det stycket visas på den slutgiltiga OneNote‑sidan och i den exporterade PDF‑filen.

## Varför exportera OneNote till PDF?

Att exportera OneNote till PDF säkerställer konsekvent varumärkesprofil genom att bevara företagets teckensnitt och färger, förbättrar läsbarheten genom att behålla exakt layout för utskrift eller arkivering, och ger plattformsoberoende åtkomst så att mottagare kan visa dokumentet på vilken enhet som helst utan att behöva OneNote. Det ger också prestandafördelar, vilket möjliggör snabb bearbetning av stora dokument.

## Förutsättningar

1. **Java Development Kit (JDK) 1.8+** – någon nyare JDK fungerar.  
2. **Aspose.Note for Java** – ladda ner den senaste JAR‑filen från [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **En IDE** (Eclipse, IntelliJ IDEA eller NetBeans) för att kompilera och köra exemplet.  

> **Pro tip:** Lägg till Aspose.Note‑JAR‑filen i ditt projekts classpath via Maven (`<dependency>`) eller genom att manuellt referera JAR‑filen i din IDE.

## Importera paket

Först importerar du de nödvändiga namnutrymmena. Detta block förblir oförändrat.

```java
import java.awt.Color;
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.Outline;
import com.aspose.note.OutlineElement;
import com.aspose.note.Page;
import com.aspose.note.RichText;
import com.aspose.note.SaveFormat;
import com.aspose.note.ParagraphStyle;
```

> `ParagraphStyle`‑klassen är nyckeln till **set paragraph style** senare i handledningen.

## Steg‑för‑steg‑guide

Nedan följer en kort genomgång av varje operation. Kodblocken är exakt som i originalexemplet; vi lägger bara till förklarande text.

### Steg 1: ange dokumentkatalog
Definiera var de genererade filerna ska sparas.

```java
String dataDir = "Your Document Directory";
```

Ersätt `"Your Document Directory"` med en absolut eller relativ sökväg på din maskin.

### Steg 2: initiera dokumentobjekt
Skapa rot‑`Document` som representerar OneNote‑filen.

```java
Document doc = new Document();
```

**Definition anchor:** `Document` är Aspose.Note:s översta objekt som håller en eller flera sidor i minnet.

### Steg 3: initiera sidobjekt
En OneNote‑fil består av en eller flera sidor; vi börjar med en enda sida.

```java
Page page = new Page();
```

**Definition anchor:** `Page` representerar en enskild OneNote‑sida som innehåller konturer, bilder och andra element.

### Steg 4: initiera konturobjekt
Konturer fungerar som behållare för konturelement (tänk på dem som sektioner).

```java
Outline outline = new Outline();
```

**Definition anchor:** `Outline` grupperar relaterade `OutlineElement`‑objekt och definierar deras visuella hierarki.

### Steg 5: initiera konturelementobjekt
Här **add outline element** som kommer att hålla vår formaterade text.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Definition anchor:** `OutlineElement` är en lövnod inom en `Outline` som kan innehålla text, bilder eller annan media.

### Steg 6: ange textstil (set paragraph style)
`ParagraphStyle` definierar teckensnittsfamilj, storlek, färg och andra typografiska attribut för ett stycke.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

`ParagraphStyle`‑instansen definierar teckensnitt, storlek och färg – här **set paragraph style** för den kommande textnoden.

### Steg 7: initiera RichText‑objekt
`RichText` är noden som lagrar formaterad text inom ett `OutlineElement`.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

Vi skapar en `RichText`‑nod, infogar en enkel sträng och bifogar den tidigare definierade stilen.

### Steg 8: lägg till RichText‑nod i OutlineElement
```java
outlineElem.appendChildLast(text);
```

Nu finns den formaterade texten inuti konturelementet.

### Steg 9: lägg till OutlineElement‑nod i Outline
```java
outline.appendChildLast(outlineElem);
```

Outline‑objektet innehåller nu elementet som håller vårt stycke.

### Steg 10: lägg till Outline‑nod på sidan
```java
page.appendChildLast(outline);
```

Vi placerar outline‑objektet på sidan.

### Steg 11: lägg till Page‑nod i dokumentet
```java
doc.appendChildLast(page);
```

Dokumentet har nu en enda sida med vår formaterade text.

### Steg 12: spara dokumentet (export OneNote PDF)
```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

`save`‑metoden skriver OneNote‑filen och **exports OneNote to PDF** i ett steg. Du kan också spara som `.one` genom att använda `SaveFormat.One` om du behöver det ursprungliga formatet.

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|---------|-------|---------|
| **File not found** | `dataDir` pekar på en icke‑existerande mapp. | Se till att katalogen finns eller skapa den programatiskt (`new File(dataDir).mkdirs();`). |
| **Blank PDF** | Inget innehåll lades till innan sparning. | Verifiera att `RichText`‑noden har lagts till och att stilen är inställd. |
| **Unsupported font** | Teckensnittet är inte installerat på systemet. | Använd ett vanligt teckensnitt som `"Arial"` eller bädda in teckensnittet i projektet. |

## Vanliga frågor

**Q: Kan Aspose.Note hantera komplex formatering såsom tabeller eller bilder?**  
A: Ja, API:et stöder tabeller, bilder, hyperlänkar och avancerade layoutfunktioner utöver vanlig text.

**Q: Är det möjligt att konvertera en OneNote‑PDF tillbaka till en OneNote‑fil?**  
A: Direkt konvertering erbjuds inte, men du kan extrahera PDF‑innehåll och återskapa ett OneNote‑dokument med hjälp av API:et.

**Q: Fungerar biblioteket på Linux/macOS‑miljöer?**  
A: Absolut. Aspose.Note för Java är plattformsoberoende; se bara till att en kompatibel JDK är installerad.

**Q: Hur lägger jag till flera sidor eller konturer?**  
A: Skapa ytterligare `Page`‑ och `Outline`‑objekt och lägg sedan till dem i `Document` på samma sätt som i enkelsidsexemplet.

**Q: Var kan jag hitta fler exempel?**  
A: Den officiella Aspose.Note‑dokumentationen och [supportforumet](https://forum.aspose.com/c/note/28) innehåller många kodexempel och verkliga scenarier.

## Slutsats

Du har nu sett hur man **set paragraph style**, **add outline element** och **export OneNote to PDF** med Aspose.Note för Java. Att applicera formaterad text tidigt säkerställer att den slutliga PDF‑filen ser professionell ut, och den enkla `save`‑metoden hanterar konverteringen effektivt. Utöka detta grundläggande exempel med bilder, tabeller eller anpassad metadata för att möta ditt programs specifika behov.

---

**Last Updated:** 2026-08-18  
**Tested With:** Aspose.Note for Java 26.5 (latest release)  
**Author:** Aspose

## Relaterade handledningar

- [Hur man sparar OneNote som PDF med Aspose.Note för Java](/note/java/onenote-document-loading/load-save-format/)
- [Lär dig konvertera OneNote till PDF med Aspose.Note med PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Ställ in standard styckeformat i OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}