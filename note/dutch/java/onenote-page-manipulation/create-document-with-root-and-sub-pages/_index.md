---
title: Maak een document met hoofd- en subpagina's in OneNote
linktitle: Maak een document met hoofd- en subpagina's in OneNote
second_title: Aspose.Note Java-API
description: Maak een document met hoofd- en subpagina's in OneNote met behulp van Aspose.Note voor Java. Volg de stapsgewijze handleiding om uw notities efficiënt te ordenen.
weight: 11
url: /nl/java/onenote-page-manipulation/create-document-with-root-and-sub-pages/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een document met hoofd- en subpagina's in OneNote

## Invoering

In deze zelfstudie begeleiden we u bij het maken van een document met hoofd- en subpagina's in OneNote met behulp van Aspose.Note voor Java. Door deze stappen te volgen, kunt u uw OneNote-documenten efficiënt ordenen met een hiërarchische structuur.

## Vereisten

Voordat u begint, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1. Java Development Kit (JDK): Zorg ervoor dat JDK op uw systeem is geïnstalleerd.
2. Aspose.Note voor Java: Download en installeer Aspose.Note voor Java vanaf de[website](https://purchase.aspose.com/buy).
3. Integrated Development Environment (IDE): Kies een Java IDE zoals IntelliJ IDEA, Eclipse of NetBeans.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten in uw Java-project:

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

Definieer de map waarin u uw OneNote-document wilt opslaan:

```java
String dataDir = "Your Document Directory";
```

## Stap 2: Maak een documentobject

 Instantieer een`Document` voorwerp:

```java
Document doc = new Document();
```

## Stap 3: Pagina's maken

Initialiseer pagina-objecten en stel hun niveaus in:

```java
Page page1 = new Page();
page1.setLevel((byte) 1);

Page page2 = new Page();
page2.setLevel((byte) 2);

Page page3 = new Page();
page3.setLevel((byte) 1);
```

## Stap 4: Voeg knooppunten toe aan pagina's

### Knooppunten toevoegen aan de eerste pagina

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

### Knooppunten toevoegen aan de tweede pagina

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

### Knooppunten toevoegen aan de derde pagina

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

## Stap 5: Pagina's toevoegen aan het document

```java
doc.appendChildLast(page1);
doc.appendChildLast(page2);
doc.appendChildLast(page3);
```

## Stap 6: Sla het document op

Sla het OneNote-document op:

```java
try {
    doc.save(dataDir + "GenerateRootAndSubLevelPagesInOneNote_out.bmp", SaveFormat.Bmp);
} catch (IOException e) {
    // Uitzondering verwerken
}
```

Gefeliciteerd! U hebt met succes een document met hoofd- en subpagina's in OneNote gemaakt met Aspose.Note voor Java.

## Conclusie

Het organiseren van uw OneNote-documenten met een hiërarchische structuur is essentieel voor beter beheer en betere navigatie. Met Aspose.Note voor Java kunt u efficiënt documenten maken met hoofd- en subpagina's, waardoor uw notities een duidelijke en georganiseerde lay-out krijgen.

## Veelgestelde vragen

### V1: Kan ik meerdere niveaus van subpagina's maken met Aspose.Note voor Java?

A1: Ja, u kunt meerdere niveaus van subpagina's maken door voor elke pagina het juiste niveau in te stellen.

### V2: Is Aspose.Note voor Java compatibel met verschillende Java-IDE's?

A2: Ja, Aspose.Note voor Java is compatibel met populaire Java IDE's zoals IntelliJ IDEA, Eclipse en NetBeans.

### V3: Kan ik de opmaak van tekst in mijn OneNote-document aanpassen?

A3: Ja, u kunt het lettertype, de kleur, de grootte en andere opmaakopties aanpassen met Aspose.Note voor de rijke tekstfuncties van Java.

### V4: Ondersteunt Aspose.Note voor Java het opslaan van documenten in verschillende formaten?

A4: Ja, Aspose.Note voor Java ondersteunt het opslaan van documenten in verschillende formaten, waaronder BMP, PDF, PNG en meer.

### V5: Is er een proefversie beschikbaar voor Aspose.Note voor Java?

A5: Ja, u kunt een gratis proefversie van Aspose.Note voor Java downloaden van de website.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
