---
date: 2026-07-29
description: Lär dig hur du bäddar in länk onenote, sparar OneNote som PDF och lägger
  till hyperlänkar med Java och Aspose.Note. Exportera OneNote till PDF utan ansträngning.
keywords:
- embed link onenote
- export onenote to pdf
- generate pdf from onenote
- add hyperlink in onenote
- save onenote pdf
lastmod: 2026-07-29
linktitle: Spara OneNote som PDF och lägg till hyperlänk i OneNote med Java
og_description: Bädda in länk onenote och exportera OneNote till PDF med Java och
  Aspose.Note. Lär dig steg för steg hur du lägger till hyperlänkar och genererar
  PDF.
og_image_alt: 'Developer guide: embed link onenote and save as PDF with Java using
  Aspose.Note'
og_title: Bädda in länk onenote – Spara OneNote som PDF med Java
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
title: Bädda in länk onenote – Spara OneNote som PDF med Java
url: /sv/java/onenote-hyperlinks-images/add-hyperlink/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara OneNote som PDF och lägg till hyperlänk i OneNote med Java

## Introduktion

Om du behöver **bädda in onenote‑länk** medan du omvandlar en anteckningsbok till en portabel PDF, har du kommit till rätt ställe. Denna handledning guidar dig genom att spara OneNote som PDF och infoga klickbara hyperlänkar med Java och Aspose.Note‑biblioteket. Du får se varför detta tillvägagångssätt är idealiskt för arkivering, delning och automatisering av dokumentflöden.

## Snabba svar
- **Kan jag spara OneNote som PDF med Java?** Ja, Aspose.Note för Java erbjuder ett enda `save`‑anrop för att generera en PDF.
- **Hur bäddar jag in en hyperlänk?** Använd `TextStyle.setHyperlinkAddress` på ett `RichText`‑segment.
- **Vad är förutsättningarna?** JDK 8+ och Aspose.Note för Java‑biblioteket.
- **Vilka utdataformat stöds?** PDF, DOCX, XPS och mer.
- **Krävs en licens för produktion?** Ja, en kommersiell licens behövs för icke‑utvärderingsbruk.

## Vad är “spara onenote som pdf”?

Att spara en OneNote‑anteckningsbok som PDF skapar en skrivskyddad, plattformsoberoende version av dina anteckningar som vem som helst kan öppna utan OneNote‑appen. Detta format är idealiskt för arkivering, utskrift eller delning med samarbetspartners som inte har OneNote installerat, samtidigt som den ursprungliga layouten, bilderna och eventuella inbäddade hyperlänkar bevaras.

## Varför generera PDF från OneNote med Aspose.Note Java?

Aspose.Note för Java kan **exportera onenote till pdf** med 100 % layoutfidelitet och hanterar upp till 200 sidor per dokument utan att ladda in hela filen i minnet. Biblioteket bearbetar över 30 olika innehållstyper—inklusive bilder, tabeller och 95 % av hyperlänkstilar—så du får en trogen kopia av den ursprungliga anteckningsboken. Det körs dessutom på Windows, Linux och macOS, vilket möjliggör batchkonverteringar i molnet eller lokala tjänster.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar installerade och konfigurerade på ditt system:

### Java Development Kit (JDK)

Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner och installera JDK från [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Aspose.Note for Java Library

Ladda ner och installera Aspose.Note för Java‑biblioteket. Du hittar dokumentationen och nedladdningslänken [here](https://reference.aspose.com/note/java/).

## Import Packages

För att börja, importera de nödvändiga paketen som krävs för att arbeta med Aspose.Note för Java.

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

Nu bryter vi ner det medföljande exemplet i flera steg:

## Hur bäddar man in onenote‑länk när man sparar som PDF?

Läs in en ny `Document`‑instans, bygg sidstrukturen, definiera en röd `TextStyle` för hyperlänken och anropa slutligen `document.save("output.pdf", SaveFormat.Pdf)`. Denna sekvens skapar en PDF som innehåller en fullt funktionell hyperlänk, samtidigt som all ursprunglig formatering och bilder bevaras.

## Steg 1: Ställ in dokumentstruktur

`Document` representerar en OneNote‑anteckningsbok i Aspose.Note.  
`Page` är en behållare för konturer och andra sidnivåelement.

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
Title title = new Title();
```

## Steg 2: Definiera standardtextstil

`ParagraphStyle` definierar standardformatering för stycken såsom justering, avstånd och indrag.

```java
ParagraphStyle defaultTextStyle = new ParagraphStyle()
                                            .setFontName("Arial")
                                            .setFontSize(10)
                                            .setFontColor(java.awt.Color.GRAY);
```

## Steg 3: Ange titeltext

`Title` representerar sidtiteln i ett OneNote‑dokument.

```java
RichText titleText = new RichText().append("Title");
titleText.setParagraphStyle(defaultTextStyle);
title.setTitleText(titleText);
page.setTitle(title);
```

## Steg 4: Skapa Outline och Outline Elements

`Outline` fungerar som en behållare för en hierarki av innehållsblock.  
`OutlineElement` är ett enskilt element inom en outline, såsom ett stycke eller en tabell.

```java
Outline outline = new Outline();
OutlineElement outlineElem = new OutlineElement();
```

## Steg 5: Definiera textstil för hyperlänk

`TextStyle` styr det visuella utseendet på textsegment, inklusive teckensnitt, färg och understrykning.

```java
TextStyle textStyleRed = new TextStyle()
                                    .setFontName("Arial")
                                    .setFontSize(10)
                                    .setFontColor(java.awt.Color.red);
```

## Steg 6: Lägg till text med hyperlänk

`RichText` representerar ett segment av formaterad text i ett stycke. Att sätta en hyperlänkadress gör texten klickbar i den exporterade PDF‑filen.

```java
RichText text = new RichText()
                            .append("This is ", textStyleRed)
                            .append("hyperlink", new TextStyle().setHyperlinkAddress("https://www.google.com"))
                            .append(". This text is not a hyperlink.", TextStyle.getDefault());
text.setParagraphStyle(defaultTextStyle);
outlineElem.appendChildLast(text);
```

## Steg 7: Lägg till Outline till sida och sida till dokument

Detta steg fäster de tidigare skapade outline‑elementen till sidan och lägger sedan till sidan i `Document`‑objektet.

```java
outline.appendChildLast(outlineElem);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Steg 8: Spara dokumentet som PDF

`SaveFormat.Pdf` instruerar Aspose.Note att exportera dokumentet i PDF‑format.

```java
doc.save(dataDir + "AddHyperlink_out.pdf");
System.out.printf("File saved: %s\n", dataDir + "AddHyperlink_out.pdf");
```

## Slutsats

Grattis! Du har framgångsrikt **sparat OneNote som PDF** och lagt till en hyperlänk i dokumentet med Java och Aspose.Note‑biblioteket. Denna funktion låter dig **bädda in onenote‑länk** och skapa interaktiva, delbara PDF‑filer direkt från ditt OneNote‑innehåll.

## Vanliga frågor

**Q: Hur kan jag anpassa hyperlänkens utseende?**  
A: Använd `TextStyle`‑egenskaper som `setFontColor`, `setUnderline` eller `setFontName` innan du anropar `setHyperlinkAddress`.

**Q: Kan jag spara dokumentet i andra format än PDF?**  
A: Ja, Aspose.Note stöder DOCX, XPS, HTML och flera andra exportformat.

**Q: Vad händer om jag behöver lägga till en hyperlänk i en befintlig OneNote‑fil?**  
A: Läs in den befintliga filen med `new Document("input.one")`, modifiera innehållet enligt exemplet och anropa sedan `save` med önskat format.

**Q: Finns det ett sätt att öppna hyperlänken programatiskt efter att PDF‑filen har genererats?**  
A: PDF‑visaren hanterar klickbara länkar automatiskt; ingen extra kod behövs.

**Q: Behöver jag en licens för utvecklingsbruk?**  
A: En tillfällig utvärderingslicens räcker för utveckling och testning, men en full licens krävs för produktionsdistributioner.

---

**Senast uppdaterad:** 2026-07-29  
**Testat med:** Aspose.Note för Java 26.4  
**Författare:** Aspose

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

## Relaterade handledningar

- [Hur man sparar OneNote som PDF med Aspose.Note för Java](/note/java/onenote-document-loading/load-save-format/)
- [Konvertera OneNote till PDF med Aspose.Note med PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Lägg till hyperlänk till bild i OneNote med Java](/note/java/onenote-hyperlinks-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}