---
date: 2025-12-09
description: Leer hoe je OneNote als PDF kunt opslaan met opgemaakte rich text in
  Java met behulp van Aspose.Note voor Java. Volg onze stapsgewijze gids voor naadloze
  documentautomatisering.
linktitle: Save OneNote as PDF with Formatted Rich Text in Java
second_title: Aspose.Note Java API
title: OneNote opslaan als PDF met opgemaakte rich‑tekst in Java
url: /nl/java/onenote-document-manipulation/create-onenote-document-formatted-rich-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OneNote opslaan als PDF met opgemaakte Rich Text in Java

## Inleiding

Als je **OneNote als PDF wilt opslaan** terwijl je de rich‑text opmaak behoudt, ben je hier aan het juiste adres. In deze tutorial lopen we door het maken van een OneNote‑document, het toepassen van aangepaste stijlen, en het direct exporteren naar PDF met Aspose.Note for Java. Aan het einde heb je een herbruikbare code‑snippet die je in elk Java‑project kunt plaatsen om gepolijste OneNote‑naar‑PDF conversies te automatiseren.

## Snelle antwoorden
- **Wat leert deze tutorial?** Hoe je een OneNote‑document maakt met gestylede tekst en het opslaat als een PDF.  
- **Welke bibliotheek is vereist?** Aspose.Note for Java (downloadbaar vanaf de officiële site).  
- **Heb ik een licentie nodig?** Een tijdelijke licentie werkt voor testen; een volledige licentie is vereist voor productie.  
- **Welke IDE kan ik gebruiken?** Elke Java‑IDE—IntelliJ IDEA, Eclipse, of NetBeans.  
- **Kan ik het uitvoerformaat wijzigen?** Ja, Aspose.Note ondersteunt PDF, HTML, PNG en meer.

## Wat betekent “OneNote opslaan als PDF”?
OneNote opslaan als PDF betekent dat je de OneNote‑pagina‑structuur—inclusief tekst, afbeeldingen en opmaak—converteert naar een statisch PDF‑bestand dat op elk platform kan worden bekeken zonder OneNote nodig te hebben.

## Waarom rich‑text opmaken in Java?
Het toepassen van rich‑text opmaak (lettertypen, kleuren, stijlen) direct in Java stelt je in staat documenten te genereren die er professioneel uitzien en voldoen aan je merkrichtlijnen zonder handmatige bewerking.

## Vereisten

1. **Java Development Kit (JDK)** – elke recente versie (8 of hoger).  
2. **Aspose.Note for Java JAR** – download deze via de [download link](https://releases.aspose.com/note/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, of elke editor die je verkiest.  

## Pakketten importeren

Allereerst moet je de benodigde pakketten importeren in je Java‑project. Voeg de volgende import‑statements toe aan het begin van je Java‑bestand:

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

## Stap 1: Document en pagina instellen

Laten we beginnen met het initialiseren van de `Document`‑ en `Page`‑objecten:

```java
String dataDir = "Your Document Directory";
Document doc = new Document();
Page page = new Page();
```

## Stap 2: Titel maken met opmaak

Nu maken we een titel met opgemaakte tekst:

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

## Stap 3: Rich Text maken met opmaak

Vervolgens maken we rich text met verschillende opmaakstijlen:

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

## Stap 4: Elementen toevoegen aan pagina en document

Nu voegen we de titel en rich text toe aan de pagina en de outline‑elementen:

```java
outlineElem.appendChildLast(text);
outline.appendChildLast(outlineElem);
page.setTitle(title);
page.appendChildLast(outline);
doc.appendChildLast(page);
```

## Stap 5: Document opslaan

Tot slot slaan we het gemaakte One‑document op als een PDF:

```java
doc.save(dataDir + "CreateOneNoteDocument_out.pdf", SaveFormat.Pdf);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Bestand niet gevonden** | Controleer of `dataDir` naar een bestaande map wijst en of je schrijfrechten hebt. |
| **Ontbrekende lettertypen** | Zorg ervoor dat de lettertypen die je gebruikt (bijv. *Calibri*) geïnstalleerd zijn op de hostmachine. |
| **Licentie niet toegepast** | Laad je Aspose‑licentie voordat je het `Document` maakt om evaluatiewatermerken te voorkomen. |

## Veelgestelde vragen

**V: Kan ik de lettertype‑stijlen verder aanpassen?**  
A: Ja, je kunt extra eigenschappen aanpassen zoals onderstrepen, doorhalen en tekstuitlijning via de `TextStyle`‑ en `ParagraphStyle`‑klassen.

**V: Is Aspose.Note for Java compatibel met alle Java‑IDE's?**  
A: Absoluut. Zolang de IDE standaard Java‑ontwikkeling ondersteunt, kun je de Aspose.Note‑JAR aan de classpath van het project toevoegen.

**V: Kan ik deze functionaliteit integreren in webapplicaties?**  
A: Ja, dezelfde code werkt in servlet‑gebaseerde of Spring Boot‑applicaties, waardoor dynamische OneNote‑naar‑PDF‑generatie aan de serverkant mogelijk is.

**V: Zijn er licentie‑vereisten voor het gebruik van Aspose.Note for Java?**  
A: Een commerciële licentie is vereist voor productiegebruik. Een tijdelijke licentie is Ondersteunt Aspose.Note for Java andere documentformaten naast OneNote?**  
A: Het ondersteunt PDF, HTML, PNG, JPEG en verschillende andere exportformaten, waardoor je flexibiliteit hebt om OneNote‑pagina's naar het gewenste formaat te converteren.

## Conclusie

In deze gids hebben we laten zien hoe je **OneNote als PDF kunt opslaan** terwijl je rich‑text opmaak toepast met Aspose.Note for Java. Door de stap‑voor‑stap instructies te volgen kun je het maken van gepolijste OneNote‑documenten automatiseren en ze omzetten naar PDF in elke Java‑gebaseerde oplossing.

---

**Laatst bijgewerkt:** 2025-12-09  
**Getest met:** Aspose.Note for Java 24.11 (latest at time of writing)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}