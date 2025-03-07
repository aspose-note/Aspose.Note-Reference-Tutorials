---
title: Opslaan in grijswaardenafbeelding in OneNote - Aspose.Note
linktitle: Opslaan in grijswaardenafbeelding in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u een document opslaat als grijswaardenafbeelding in OneNote met behulp van Aspose.Note voor Java. Bewerk eenvoudig Microsoft OneNote-documenten programmatisch.
weight: 17
url: /nl/java/onenote-document-saving/save-to-grayscale-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan in grijswaardenafbeelding in OneNote - Aspose.Note

## Invoering

In deze zelfstudie onderzoeken we hoe u een document als grijswaardenafbeelding in OneNote kunt opslaan met Aspose.Note voor Java. Grijswaardenafbeeldingen zijn monochrome afbeeldingen waarbij de kleurinformatie alleen door grijstinten wordt weergegeven. Aspose.Note is een krachtige Java API die programmatische manipulatie van Microsoft OneNote-documenten mogelijk maakt.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

1. Java Development Kit (JDK) op uw systeem geïnstalleerd.
2.  Aspose.Note voor Java-bibliotheek. Je kunt het downloaden van[hier](https://releases.aspose.com/note/java/).
3. Basiskennis van Java-programmeren.

## Pakketten importeren

Importeer de benodigde pakketten om aan de slag te gaan:

```java
import com.aspose.note.ColorMode;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
import java.io.IOException;
```

## Stap 1: Laad het document

 Laad eerst het document in Aspose.Note. Vervangen`"Your Document Directory"` met het pad naar uw documentmap en`"Aspose.one"` met de naam van uw OneNote-document.

```java
String dataDir = "Your Document Directory";
Document oneFile = new Document(dataDir + "Aspose.one");
```

## Stap 2: Stel het uitvoerpad en de opties in

Definieer het uitvoerpad voor de grijswaardenafbeelding en geef de opslagopties op. We stellen de kleurmodus in op grijswaarden.

```java
dataDir = dataDir + "SaveAsGrayscaleImage_out.png";
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.setColorMode(ColorMode.GrayScale);
```

## Stap 3: Sla het document op

Sla het document ten slotte op als een grijswaardenafbeelding met behulp van de opgegeven opties.

```java
oneFile.save(dataDir, options);
```

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u een document kunt opslaan als grijswaardenafbeelding in OneNote met behulp van Aspose.Note voor Java. Dit kan ongelooflijk handig zijn voor verschillende toepassingen waarbij grijswaardenafbeeldingen vereist zijn.

## Veelgestelde vragen

### Vraag 1: Kan ik de grijswaardenafbeelding in een ander formaat opslaan?

 A1: Ja, dat kan. Verander eenvoudigweg de`SaveFormat` parameter in de`ImageSaveOptions` constructor naar het gewenste formaat.

### V2: Is Aspose.Note compatibel met alle versies van OneNote-documenten?

A2: Aspose.Note ondersteunt Microsoft OneNote 2010 en hoger.

### V3: Heeft Aspose.Note een licentie nodig om te gebruiken?

A3: Ja, u heeft een geldige licentie nodig om Aspose.Note in productieomgevingen te gebruiken. U kunt echter wel een tijdelijke licentie verkrijgen voor testdoeleinden.

### V4: Kan ik andere aspecten van het document manipuleren voordat ik het als afbeelding opsla?

A4: Absoluut! Aspose.Note biedt een breed scala aan functies voor het programmatisch bewerken van OneNote-documenten.

### Vraag 5: Waar kan ik ondersteuning vinden als ik problemen tegenkom?

A5: U kunt ondersteuning vinden op het Aspose.Note-forum[hier](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
