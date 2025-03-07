---
title: Converteer OneNote-document naar afbeelding - Java
linktitle: Converteer OneNote-document naar afbeelding - Java
second_title: Aspose.Note Java-API
description: Leer hoe u OneNote naar een afbeelding kunt converteren met Aspose.Note voor Java. Volg eenvoudige stappen, laad het document, initialiseer opties en sla het op als PNG.
weight: 14
url: /nl/java/onenote-document-loading/convert-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Converteer OneNote-document naar afbeelding - Java

## Invoering

In deze zelfstudie begeleiden we u bij het gebruik van Aspose.Note voor Java om een OneNote-document naar een afbeelding te converteren. We zullen elke stap opsplitsen in eenvoudig te volgen instructies.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

1. Java Development Kit (JDK) op uw systeem geïnstalleerd.
2.  Aspose.Note voor Java-bibliotheek. Je kunt het downloaden van[hier](https://releases.aspose.com/note/java/).

## Pakketten importeren

Importeer eerst de benodigde pakketten in uw Java-code:

```java
import java.io.IOException;
import com.aspose.note.Document;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.SaveFormat;
```

Laten we nu de voorbeeldcode in meerdere stappen opsplitsen:

## Stap 1: Documentmap instellen

Definieer de map waarin uw OneNote-document zich bevindt:

```java
String dataDir = "Your Document Directory";
```

 Vervangen`"Your Document Directory"` met het pad naar uw OneNote-document.

## Stap 2: Laad het document

Laad het OneNote-document in Aspose.Note:

```java
Document oneFile = new Document(dataDir + "Sample1.one");
```

 Ervoor zorgen`"Sample1.one"` komt overeen met de naam van uw OneNote-documentbestand.

## Stap 3: Initialiseer ImageSaveOptions

 Initialiseer de`ImageSaveOptions` object om het opslagformaat op te geven:

```java
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
```

Hier slaan we het document op als een PNG-afbeelding. U kunt indien nodig andere formaten kiezen, zoals JPEG of BMP.

## Stap 4: Sla het document op als afbeelding

Sla het geladen document op als afbeelding:

```java
oneFile.save(dataDir + "ConvertToImage_out.png", options);
```

Deze regel slaat het document op als een PNG-afbeelding met de opgegeven opties.

## Stap 5: Bevestiging afdrukken

Druk een bericht af om te bevestigen dat het bestand is opgeslagen:

```java
System.out.println("File saved: " + dataDir + "ConvertToImage_out.png");
```

Deze regel informeert u over de succesvolle conversie en de locatie van het opgeslagen afbeeldingsbestand.

## Conclusie

Door de hierboven beschreven stappen te volgen, kunt u een OneNote-document moeiteloos naar een afbeelding converteren met Aspose.Note voor Java. Het is een eenvoudige en effectieve manier om documentconversies in uw Java-toepassingen af te handelen.

## Veelgestelde vragen

### V1: Kan ik meerdere OneNote-documenten in één keer converteren?

A1: Ja, u kunt een lijst met documenten doorlopen en de conversiebewerking voor elk document uitvoeren.

### V2: Ondersteunt Aspose.Note andere uitvoerformaten dan afbeeldingen?

A2: Ja, Aspose.Note ondersteunt verschillende uitvoerformaten, zoals PDF-, HTML- en Microsoft Word-formaten.

### V3: Is Aspose.Note compatibel met alle versies van OneNote-bestanden?

A3: Aspose.Note biedt compatibiliteit met OneNote-bestanden die in verschillende versies van Microsoft OneNote zijn gemaakt.

### Vraag 4: Kan ik de resolutie van de uitvoerafbeeldingen aanpassen?

A4: Ja, u kunt de resolutie en andere parameters aanpassen met behulp van de opties die beschikbaar zijn in Aspose.Note.

### V5: Heeft Aspose.Note een internetverbinding nodig voor documentconversie?

A5: Nee, Aspose.Note werkt lokaal zonder dat er een internetverbinding nodig is.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
