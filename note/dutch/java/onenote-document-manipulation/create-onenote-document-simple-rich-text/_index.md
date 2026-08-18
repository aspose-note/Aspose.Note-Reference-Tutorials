---
date: 2026-08-18
description: Leer hoe je OneNote naar PDF exporteert, paragraph formatting instelt
  in Java, en OneNote opslaat als PDF met Aspose.Note voor Java.
keywords:
- export onenote to pdf
- save onenote as pdf
- paragraph formatting java
- rich text formatting java
- aspose note java
lastmod: 2026-08-18
linktitle: Paragraph Style instellen tijdens het maken van een OneNote-document in
  Java
og_description: Export OneNote naar PDF en stel paragraph style in Java in met Aspose.Note.
  Volg deze step‑by‑step gids om moeiteloos gepolijste PDF's te genereren.
og_image_alt: Screenshot of Java code exporting OneNote to PDF with styled paragraphs
og_title: Export OneNote naar PDF met paragraph style in Java (58 tekens)
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
title: Hoe OneNote naar PDF exporteren met paragraph style in Java
url: /nl/java/onenote-document-manipulation/create-onenote-document-simple-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Paragraafstijl instellen bij het maken van een OneNote-document in Java

## Inleiding

Het programmatisch exporteren van OneNote naar PDF is een veelvoorkomende eis voor rapportage‑engines, geautomatiseerde notitieservices en document‑conversiepijplijnen. In deze tutorial leer je hoe je **OneNote naar PDF exporteert**, aangepaste alinea‑opmaak toepast en het OneNote‑bestand opslaat — alles met Aspose.Note voor Java. Aan het einde heb je een kant‑klaar Java‑fragment dat een gepolijste PDF produceert met precies de uitstraling die je hebt gedefinieerd.

## Snelle antwoorden
- **Wat betekent “set paragraph style”?** Het past lettertype, grootte, kleur en andere opmaak‑attributen toe op een alinea tekst.  
- **Kan ik het resultaat exporteren naar PDF?** Ja — de handleiding eindigt met het opslaan van het OneNote‑bestand als PDF.  
- **Heb ik een licentie nodig voor Aspose.Note?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productiegebruik.  
- **Welke IDE's worden ondersteund?** Elke Java‑IDE — Eclipse, IntelliJ IDEA, NetBeans, enz.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisdocument.

## Hoe OneNote exporteren naar PDF in Java?

`Document` vertegenwoordigt een OneNote‑bestand met pagina’s, outlines en andere elementen. Laad je OneNote‑document met `new Document()` (of maak een nieuw document) en roep `document.save("output.pdf", SaveFormat.Pdf)` aan. Aspose.Note schrijft de PDF in één stap, behoudt stijlen, afbeeldingen en outlines zonder dat Microsoft OneNote geïnstalleerd hoeft te zijn. Deze directe aanpak werkt op Windows, Linux en macOS met elke JDK 1.8+.

## Wat is “set paragraph style” in Aspose.Note?

`ParagraphStyle` is de klasse die lettertype, grootte, kleur, uitlijning en andere typografische instellingen voor een alinea opslaat. Door een `ParagraphStyle`‑instantie aan een `RichText`‑node te koppelen, bepaal je precies hoe die alinea eruitziet in de uiteindelijke OneNote‑pagina en de geëxporteerde PDF.

## Waarom OneNote exporteren naar PDF?

Exporteren naar PDF zorgt voor consistente branding door bedrijfslettertypen en -kleuren te behouden, verbetert de leesbaarheid door de exacte lay‑out te behouden voor afdrukken of archivering, en biedt cross‑platform toegang zodat ontvangers het document op elk apparaat kunnen bekijken zonder OneNote. Het biedt bovendien prestatievoordelen, waardoor grote documenten snel verwerkt kunnen worden.

## Voorvereisten

1. **Java Development Kit (JDK) 1.8+** – elke recente JDK werkt.  
2. **Aspose.Note for Java** – download de nieuwste JAR van de [Aspose.Note download page](https://releases.aspose.com/note/java/).  
3. **Een IDE** (Eclipse, IntelliJ IDEA of NetBeans) om het voorbeeld te compileren en uit te voeren.  

> **Pro tip:** Voeg de Aspose.Note‑JAR toe aan de classpath van je project via Maven (`<dependency>`) of door handmatig de JAR in je IDE te refereren.

## Pakketten importeren

Eerst importeer je de benodigde namespaces. Dit blok blijft ongewijzigd.

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

> De `ParagraphStyle`‑klasse is de sleutel om later in de tutorial **set paragraph style** toe te passen.

## Stapsgewijze handleiding

Hieronder vind je een beknopte walkthrough van elke bewerking. De code‑blokken zijn exact zoals in het originele voorbeeld; we voegen alleen verklarende tekst toe.

### Stap 1: documentmap instellen
Definieer waar de gegenereerde bestanden worden opgeslagen.

```java
String dataDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door een absoluut of relatief pad op uw machine.

### Stap 2: documentobject initialiseren
Maak het root‑`Document` dat het OneNote‑bestand vertegenwoordigt.

```java
Document doc = new Document();
```

**Definitie‑anker:** `Document` is het top‑level object van Aspose.Note dat één of meer pagina’s in het geheugen houdt.

### Stap 3: paginaobject initialiseren
Een OneNote‑bestand bestaat uit één of meer pagina’s; we beginnen met één pagina.

```java
Page page = new Page();
```

**Definitie‑anker:** `Page` vertegenwoordigt een enkele OneNote‑pagina, met outlines, afbeeldingen en andere elementen.

### Stap 4: outline‑object initialiseren
Outlines fungeren als containers voor outline‑elementen (denk aan secties).

```java
Outline outline = new Outline();
```

**Definitie‑anker:** `Outline` groepeert gerelateerde `OutlineElement`‑objecten en definieert hun visuele hiërarchie.

### Stap 5: outline‑elementobject initialiseren
Hier **voegen we een outline‑element toe** dat onze rich‑text zal bevatten.

```java
OutlineElement outlineElem = new OutlineElement();
```

**Definitie‑anker:** `OutlineElement` is een blad‑node binnen een `Outline` die tekst, afbeeldingen of andere media kan bevatten.

### Stap 6: tekststijl instellen (set paragraph style)

`ParagraphStyle` definieert lettertypefamilie, grootte, kleur en andere typografische attributen voor een alinea.

```java
ParagraphStyle textStyle = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Arial")
                                    .setFontSize(10);
```

De `ParagraphStyle`‑instantie bepaalt het lettertype, de grootte en de kleur — hier stellen we **set paragraph style** in voor de komende tekst‑node.

### Stap 7: rich‑text‑object initialiseren

`RichText` is de node die gestylede tekst binnen een `OutlineElement` opslaat.

```java
RichText text = new RichText().append("Hello OneNote text!");
text.setParagraphStyle(textStyle);
```

We maken een `RichText`‑node, voegen een eenvoudige string toe en koppelen de eerder gedefinieerde stijl.

### Stap 8: rich‑text‑knooppunt toevoegen aan outline‑element

```java
outlineElem.appendChildLast(text);
```

Nu bevindt de gestylede tekst zich binnen het outline‑element.

### Stap 9: outline‑elementknooppunt toevoegen aan outline

```java
outline.appendChildLast(outlineElem);
```

De outline bevat nu het element dat onze alinea houdt.

### Stap 10: outline‑knooppunt toevoegen aan pagina

```java
page.appendChildLast(outline);
```

We plaatsen de outline op de pagina.

### Stap 11: pagina‑knooppunt toevoegen aan document

```java
doc.appendChildLast(page);
```

Het document heeft nu één pagina met onze gestylede tekst.

### Stap 12: document opslaan (OneNote PDF exporteren)

```java
doc.save(dataDir + "CreateOneNoteDocumentWithSimpleRichText_out.pdf", SaveFormat.Pdf);
```

De `save`‑methode schrijft het OneNote‑bestand en **exporteert OneNote naar PDF** in één stap. Je kunt ook opslaan als `.one` door `SaveFormat.One` te gebruiken als je het native formaat nodig hebt.

## Veelvoorkomende problemen & oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **Bestand niet gevonden** | `dataDir` wijst naar een niet‑bestaande map. | Zorg ervoor dat de map bestaat of maak deze programmatisch aan (`new File(dataDir).mkdirs();`). |
| **Lege PDF** | Er is geen inhoud toegevoegd vóór het opslaan. | Controleer of het `RichText`‑knooppunt is toegevoegd en de stijl is ingesteld. |
| **Niet‑ondersteund lettertype** | Lettertype niet geïnstalleerd op het systeem. | Gebruik een algemeen lettertype zoals `"Arial"` of embed het lettertype in het project. |

## Veelgestelde vragen

**Q: Kan Aspose.Note complexe opmaak zoals tabellen of afbeeldingen verwerken?**  
A: Ja, de API ondersteunt tabellen, afbeeldingen, hyperlinks en geavanceerde lay‑outfuncties naast platte tekst.

**Q: Is het mogelijk om een OneNote‑PDF terug te converteren naar een OneNote‑bestand?**  
A: Directe conversie wordt niet aangeboden, maar u kunt PDF‑inhoud extraheren en een OneNote‑document opnieuw opbouwen met de API.

**Q: Werkt de bibliotheek op Linux/macOS-omgevingen?**  
A: Absoluut. Aspose.Note for Java is platform‑onafhankelijk; zorg er alleen voor dat een compatibele JDK is geïnstalleerd.

**Q: Hoe voeg ik meerdere pagina's of outlines toe?**  
A: Maak extra `Page`‑ en `Outline`‑objecten aan en voeg ze vervolgens toe aan het `Document`, net als in het voorbeeld met één pagina.

**Q: Waar kan ik meer voorbeelden vinden?**  
A: De officiële Aspose.Note‑documentatie en het [ondersteuningsforum](https://forum.aspose.com/c/note/28) bevatten veel code‑voorbeelden en praktijkscenario's.

## Conclusie

Je hebt nu gezien hoe je **set paragraph style**, **outline‑element toevoegen** en **OneNote naar PDF exporteren** kunt doen met Aspose.Note voor Java. Het vroegtijdig toepassen van gestylede tekst zorgt ervoor dat de uiteindelijke PDF er professioneel uitziet, en de enkele‑aanroep `save`‑operatie handelt de conversie efficiënt af. Breid deze basis uit met afbeeldingen, tabellen of aangepaste metadata om te voldoen aan de specifieke behoeften van jouw applicatie.

---

**Laatst bijgewerkt:** 2026-08-18  
**Getest met:** Aspose.Note for Java 26.5 (latest release)  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Hoe OneNote opslaan als PDF met Aspose.Note voor Java](/note/java/onenote-document-loading/load-save-format/)
- [Leer OneNote converteren naar PDF met Aspose.Note met PdfSaveOptions](/note/java/onenote-document-loading/load-pdf-save-options/)
- [Standaard paragraafstijl instellen in OneNote - Aspose.Note](/note/java/onenote-styles/set-default-paragraph-style/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}