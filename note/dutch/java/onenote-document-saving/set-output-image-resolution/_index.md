---
title: Stel de resolutie van de uitvoerafbeelding in OneNote in - Aspose.Note
linktitle: Stel de resolutie van de uitvoerafbeelding in OneNote in - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u de afbeeldingsresolutie in OneNote-documenten kunt aanpassen met Aspose.Note voor Java. Volg onze stapsgewijze handleiding voor een eenvoudige implementatie
weight: 23
url: /nl/java/onenote-document-saving/set-output-image-resolution/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stel de resolutie van de uitvoerafbeelding in OneNote in - Aspose.Note

## Invoering

Wilt u de resolutie van afbeeldingen in uw OneNote-documenten manipuleren met Java? Aspose.Note voor Java biedt een robuuste oplossing voor dergelijke taken. In deze zelfstudie doorlopen we de stappen om de resolutie van de uitvoerafbeelding in te stellen met Aspose.Note.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

1. Java Development Kit (JDK): Installeer JDK op uw systeem.
2. Aspose.Note voor Java: Download en installeer Aspose.Note voor Java vanaf de[website](https://releases.aspose.com/note/java/).
3. Integrated Development Environment (IDE): Kies de IDE van uw voorkeur, zoals Eclipse of IntelliJ IDEA.

## Pakketten importeren

Importeer in uw Java-project de benodigde Aspose.Note-pakketten:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Stap 1: Laad het OneNote-document

Begin met het laden van het OneNote-document in uw Java-toepassing:

```java
String dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "Sample1.one");
```

 Vervangen`"Your Document Directory"` met de daadwerkelijke map waarin uw OneNote-document zich bevindt.

## Stap 2: Stel de opties voor het opslaan van afbeeldingen in

Definieer de opties voor het opslaan van afbeeldingen en geef de gewenste resolutie op:

```java
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
imageSaveOptions.setResolution(120);
```

 Hier stellen we de resolutie in op`120 dpi`. U kunt deze waarde aanpassen aan uw wensen.

## Stap 3: Sla het document op met aangepaste resolutie

Sla het document op met de bijgewerkte afbeeldingsresolutie:

```java
doc.save(dataDir + "SetOutputImageResolution_out.jpeg", imageSaveOptions);
```

Hierdoor wordt het gewijzigde document met de opgegeven resolutie opgeslagen.

## Conclusie

In deze zelfstudie hebben we onderzocht hoe u de resolutie van de uitvoerafbeelding in OneNote-documenten kunt instellen met Aspose.Note voor Java. Door deze eenvoudige stappen te volgen, kunt u de resolutie van afbeeldingen efficiënt manipuleren om aan de vereisten van uw toepassing te voldoen.


## Veelgestelde vragen

### Vraag 1: Kan ik de beeldresolutie aanpassen naar een waarde hoger dan 120 dpi?

A1: Ja, u kunt de resolutie naar wens instellen op elke gewenste waarde.

### V2: Ondersteunt Aspose.Note andere afbeeldingsformaten dan JPEG?

A2: Ja, Aspose.Note ondersteunt verschillende afbeeldingsformaten zoals PNG, BMP, GIF, enz.

### V3: Is Aspose.Note compatibel met alle versies van Java?

A3: Aspose.Note is compatibel met Java 1.6 of latere versies.

### V4: Kan ik andere aspecten van afbeeldingen in OneNote-documenten manipuleren met Aspose.Note?

A4: Ja, Aspose.Note biedt uitgebreide functies voor beeldmanipulatie, inclusief formaat wijzigen, bijsnijden en roteren.

### V5: Waar kan ik ondersteuning krijgen voor Aspose.Note-gerelateerde vragen?

 A5: U kunt hulp zoeken op het Aspose.Note-communityforum[hier](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
