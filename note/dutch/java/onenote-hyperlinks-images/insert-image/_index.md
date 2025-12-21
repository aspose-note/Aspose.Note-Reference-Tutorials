---
date: 2025-12-21
description: Leer hoe u afbeeldingen kunt toevoegen aan OneNote‑documenten met Java
  en Aspose.Note voor Java. Volg onze stapsgewijze handleiding om afbeeldingen in
  te voegen en optioneel OneNote op te slaan als PDF.
linktitle: Insert an Image in OneNote Document with Java
second_title: Aspose.Note Java API
title: Hoe een afbeelding toe te voegen aan OneNote met Java
url: /nl/java/onenote-hyperlinks-images/insert-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Insert an Image in OneNote Document with Java

## Introduction

In deze tutorial verkennen we hoe je een afbeelding in een OneNote-document kunt invoegen met Java met behulp van Aspose.Note for Java. Aspose.Note for Java is een krachtige bibliotheek die ontwikkelaars in staat stelt om programmatically met Microsoft OneNote-bestanden te werken, waardoor verschillende bewerkingen mogelijk zijn, zoals het maken, lezen en manipuleren van OneNote-documenten.

## Quick Answers
- **What is the easiest way to add image to OneNote using Java?**  
  Gebruik de `Image`‑klasse van Aspose.Note for Java en voeg deze toe aan een pagina.
- **Do I need a license for production use?**  
  Ja, een commerciële licentie is vereist voor productie‑implementaties.
- **Can I set custom dimensions for the image?**  
  Absoluut – roep `setWidth()` en `setHeight()` aan op het `Image`‑object.
- **Is it possible to save the OneNote file as PDF after adding the image?**  
  Ja, roep `save(..., SaveFormat.Pdf)` aan om **OneNote op te slaan als PDF**.
- **Which Java version is supported?**  
  Aspose.Note for Java werkt met JDK 8 en hoger.

## How to add image to OneNote using Java?

Voordat we in de code duiken, laten we kort bespreken waarom je programmatically afbeeldingen in OneNote zou willen insluiten. Of je nu notulen maakt, geautomatiseerde rapporten genereert, of een documentatie‑pipeline bouwt, het invoegen van afbeeldingen geeft je notities een visuele context die platte tekst niet kan bieden. Met Aspose.Note for Java kun je dit volledig in code doen, zonder de OneNote‑UI te openen.

## Prerequisites

Voordat we beginnen, zorg ervoor dat je de volgende vereisten hebt ingesteld:

### 1. Java Development Kit (JDK)
Zorg ervoor dat je Java Development Kit (JDK) op je systeem hebt geïnstalleerd. Je kunt JDK downloaden en installeren vanaf de Oracle‑website.

### 2. Aspose.Note for Java Library
Download en installeer de Aspose.Note for Java‑bibliotheek door de [documentatie](https://reference.aspose.com/note/java/) te volgen.

## Import Packages

Begin met het importeren van de benodigde pakketten in je Java‑project. Deze pakketten omvatten de Aspose.Note‑bibliotheek en andere vereiste afhankelijkheden.

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.HorizontalAlignment;
import com.aspose.note.Image;
import com.aspose.note.LoadOptions;
import com.aspose.note.Page;
import com.aspose.note.SaveFormat;
```

Laten we het proces van het invoegen van een afbeelding in een OneNote‑document opsplitsen in meerdere stappen:

## Step 1: Load the OneNote Document

Eerst laad je het OneNote‑document waarin je de afbeelding wilt invoegen.

```java
LoadOptions options = new LoadOptions();
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Sample1.one", options);
```

## Step 2: Get the Page

Verkrijg de pagina in het document waar je de afbeelding wilt invoegen.

```java
Page page = oneFile.getFirstChild();
```

## Step 3: Load the Image

Laad de afbeelding die je wilt invoegen in het OneNote‑document.

```java
Image image = new Image(oneFile, dataDir + "Input.jpg");
```

## Step 4: Customize Image Attributes (Optional)

Optioneel kun je de grootte, locatie en uitlijning van de afbeelding aanpassen volgens je vereisten. Dit is waar je **afbeeldingsafmetingen instelt Java** stijl.

```java
image.setWidth(100);
image.setHeight(100);
image.setVerticalOffset(400);
image.setHorizontalOffset(100);
image.setAlignment(HorizontalAlignment.Right);
```

## Step 5: Add Image to the Page

Voeg de afbeelding toe aan de pagina in het OneNote‑document.

```java
page.appendChildLast(image);
```

## Step 6: Save the Document

Sla het gewijzigde document op, inclusief de ingevoegde afbeelding. Je kunt ook **OneNote opslaan als PDF** in deze fase.

```java
try {
    oneFile.save(dataDir + "InsertanImage_out.pdf", SaveFormat.Pdf);
} catch (IOException e) {
    e.printStackTrace();
}
```

## Conclusion

In deze tutorial hebben we geleerd hoe je een afbeelding in een OneNote‑document kunt invoegen met Java met behulp van de Aspose.Note for Java‑bibliotheek. Door de stapsgewijze gids te volgen, kun je moeiteloos afbeeldingen programmatically in je OneNote‑documenten opnemen.

## FAQ's

### Q1: Can I insert multiple images into a single OneNote document using this method?

**A1:** Ja, je kunt meerdere afbeeldingen in één OneNote‑document invoegen door het proces dat in deze tutorial wordt beschreven voor elke afbeelding te herhalen.

### Q2: Is Aspose.Note for Java compatible with all versions of OneNote?

**A2:** Aspose.Note for Java ondersteunt het werken met OneNote‑bestanden die zijn gemaakt in Microsoft OneNote 2010 en latere versies.

### Q3: Can I insert images of different formats, such as PNG or GIF, into a OneNote document?

**A3:** Ja, Aspose.Note for Java ondersteunt het invoegen van afbeeldingen in diverse formaten, waaronder PNG, JPEG, GIF en meer.

### Q4: Is there a trial version of Aspose.Note for Java available for testing purposes?

**A4:** Ja, je kunt een gratis proefversie van Aspose.Note for Java downloaden van de website voor evaluatiedoeleinden.

### Q5: How can I get technical support for Aspose.Note for Java?

**A5:** Je kunt technische ondersteuning voor Aspose.Note for Java krijgen door het [forum](https://forum.aspose.com/c/note/28) te bezoeken dat gewijd is aan Aspose.Note‑producten.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.Note for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}