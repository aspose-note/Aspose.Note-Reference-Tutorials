---
description: Leer hoe u OneNote‑PDF's kunt opslaan en subpagina's kunt toevoegen in
  OneNote met Aspose.Note voor Java. Volg deze stapsgewijze handleiding om uw notities
  efficiënt te organiseren.
linktitle: How to Save OneNote PDF and Add Sub Pages
second_title: Aspose.Note Java API
title: Hoe OneNote PDF op te slaan en subpagina's toe te voegen
url: /nl/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe OneNote PDF op te slaan en subpagina's toe te voegen

## Introductie

In deze tutorial ontdek je **hoe je OneNote PDF kunt opslaan** terwijl je een document maakt dat zowel hoofd‑ als subpagina's bevat met Aspose.Note for Java. Het organiseren van je OneNote‑notitieblokken met een duidelijke hiërarchie maakt navigatie moeiteloos, en de mogelijkheid om te exporteren naar PDF zorgt ervoor dat je notities kunt delen in een universeel leesbaar formaat. We laten je ook zien hoe je **subpagina's onenote‑stijl** kunt toevoegen, zodat je met gemak meerlagige structuren kunt opbouwen.

## Snelle antwoorden
- **Wat betekent het primaire zoekwoord?** Het verwijst naar het exporteren van een OneNote‑notitieblok naar PDF met Aspose.Note.
- **Welke API wordt gebruikt?** Aspose.Note for Java.
- **Kan ik hiërarchische pagina's maken?** Ja – stel het paginaniveau in om hoofd‑ en subpagina's te bouwen.
- **Heb ik een licentie nodig?** Een gratis proefversie is beschikbaar; een commerciële licentie is vereist voor productie.
- **Welke uitvoerformaten worden ondersteund?** BMP, PDF, PNG en meer.

## Wat is “hoe OneNote PDF op te slaan”?
OneNote opslaan als PDF zet de pagina's van het notitieblok om in een vast‑layout document dat opmaak, afbeeldingen en hiërarchie behoudt. Dit is ideaal voor het delen, archiveren of afdrukken van notities.

## Waarom subpagina's onenote toevoegen?
Het toevoegen van subpagina's stelt je in staat gerelateerde inhoud onder een bovenliggende pagina te groeperen, vergelijkbaar met een map‑structuur. Het verbetert de organisatie van notities, maakt zoeken sneller en verbetert de leeservaring wanneer het notitieblok wordt geëxporteerd naar PDF.

## Voorvereisten

Voordat je begint, zorg dat je de volgende voorvereisten hebt:

1. Java Development Kit (JDK): Zorg ervoor dat je JDK op je systeem geïnstalleerd hebt.  
2. Aspose.Note for Java: Download en installeer Aspose.Note for Java vanaf de [website](https://purchase.aspose.com/buy).  
3. Integrated Development Environment (IDE): Kies een Java‑IDE zoals IntelliJ IDEA, Eclipse of NetBeans.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten in je Java‑project:

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

## Stap 1: Documentmap instellen

Definieer de map waarin je je OneNote‑document wilt opslaan:

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Documentobject maken

Instantieer een `Document`‑object:

```java
Document doc = new Document();
```

## Stap 3: Pagina's maken

Initialiseer paginobjecten en stel hun niveaus in. Het instellen van het niveau bepaalt of een pagina een hoofd‑ of een subpagina is:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Stap 4: Nodes aan pagina's toevoegen

### Nodes aan de eerste pagina toevoegen

```java
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
```

### Nodes aan de tweede pagina toevoegen

```java
Outline outline2 = new Outline();
OutlineElement outlineElem2 = new OutlineElement();
ParagraphStyle textStyle2 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("David Transparent")
                                    .setFontSize(10);

RichText text2 = new RichText().append("Second page.");
text2.setParagraphStyle(textStyle2);

outlineElem2.appendChildLast(text2);
outline2.appendChildLast(outlineElem2);
page2.appendChildLast(outline2);
```

### Nodes aan de derde pagina toevoegen

```java
Outline outline3 = new Outline();
OutlineElement outlineElem3 = new OutlineElement();
ParagraphStyle textStyle3 = new ParagraphStyle()
                                    .setFontColor(Color.black)
                                    .setFontName("Broadway")
                                    .setFontSize(10);

RichText text3 = new RichText().append("Third page.");
text3.setParagraphStyle(textStyle3);

outlineElem3.appendChildLast(text3);
outline3.appendChildLast(outlineElem3);
page3.appendChildLast(outline3);
```

## Stap 5: Pagina's aan het document toevoegen

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Stap 6: Het document opslaan

Sla het OneNote‑document op als een PDF (of BMP in dit voorbeeld). Door `SaveFormat` te wijzigen kun je exporteren naar PDF, wat voldoet aan de “hoe OneNote PDF op te slaan” vereiste:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Handle exception
}
```

> **Pro tip:** Om direct naar PDF te exporteren, vervang `SaveFormat.Bmp` door `SaveFormat.Pdf`.

Gefeliciteerd! Je hebt met succes een OneNote‑document met hoofd‑ en subpagina's gemaakt en geleerd **hoe OneNote PDF op te slaan** met Aspose.Note for Java.

## Waarom dit belangrijk is

- **Hiërarchische organisatie:** Hoofd‑ en subpagina's laten je mapstructuren nabootsen binnen OneNote.  
- **Naadloze PDF‑export:** Zodra de structuur is opgezet, behoudt exporteren naar PDF de hiërarchie, waardoor het einddocument gemakkelijk leesbaar en deelbaar is.  
- **Automatisering:** De code kan worden geïntegreerd in grotere Java‑applicaties, waardoor batch‑creatie van gestructureerde notitieblokken mogelijk is.

## Veelvoorkomende valkuilen & hoe ze te vermijden

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| Pagina's verschijnen op hetzelfde niveau | Onjuiste `setLevel`‑waarde | Gebruik `setLevel((byte) 1)` voor hoofd‑pagina's en `setLevel((byte) 2)` (of hoger) voor sub‑pagina's. |
| PDF‑output is leeg | Ontbrekende `SaveFormat.Pdf` of onjuiste bestands‑pad | Controleer of de map bestaat en gebruik `SaveFormat.Pdf`. |
| Lettertype niet toegepast | Verkeerde lettertype‑naam of ontbrekend lettertype op het systeem | Zorg ervoor dat het lettertype (bijv. “David Transparent”) geïnstalleerd is op de machine die de code uitvoert. |

## Veelgestelde vragen

**V: Kan ik meerdere niveaus van sub‑pagina's maken met Aspose.Note for Java?**  
A: Ja, je kunt diepere hiërarchieën creëren door hogere niveau‑nummers in te stellen (bijv. `setLevel((byte) 3)` voor een sub‑pagina op derde niveau).

**V: Is Aspose.Note for Java compatibel met verschillende Java‑IDE's?**  
A: Absoluut. Het werkt met IntelliJ IDEA, Eclipse, NetBeans en elke IDE die Java‑ontwikkeling ondersteunt.

**V: Kan ik de opmaak van tekst in mijn OneNote‑document aanpassen?**  
A: Ja. Gebruik `ParagraphStyle` om lettertype, grootte, kleur en andere attributen voor elk `RichText`‑element in te stellen.

**V: Ondersteunt Aspose.Note for Java het opslaan van documenten in andere formaten dan BMP?**  
A: Ja. Ondersteunde formaten omvatten PDF, PNG, JPEG, DOCX en meer. Pas de `SaveFormat`‑enum dienovereenkomstig aan.

**V: Is er een proefversie beschikbaar voor Aspose.Note for Java?**  
A: Ja, je kunt een gratis proefversie downloaden van de Aspose‑website.

## Conclusie

Het organiseren van je OneNote‑notitieblokken met een duidelijke hiërarchische structuur en het exporteren ervan als PDF maakt je notities toegankelijker en deelbaarder. Door de bovenstaande stappen te volgen, weet je nu **hoe je OneNote PDF opslaat** en **subpagina's onenote‑stijl** programmatically kunt toevoegen met Aspose.Note for Java.

---

**Laatst bijgewerkt:** 2026-01-07  
**Getest met:** Aspose.Note for Java 24.11 (latest)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}