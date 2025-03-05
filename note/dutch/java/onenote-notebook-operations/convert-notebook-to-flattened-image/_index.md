---
title: Converteer Notebook naar afgeplatte afbeelding in OneNote - Aspose.Note
linktitle: Converteer Notebook naar afgeplatte afbeelding in OneNote - Aspose.Note
second_title: Aspose.Note Java-API
description: Leer hoe u een notitieblok converteert naar een afgeplatte afbeelding in OneNote met behulp van Aspose.Note voor Java. Bewaar moeiteloos alle elementen in één afbeeldingsbestand.
type: docs
weight: 13
url: /nl/java/onenote-notebook-operations/convert-notebook-to-flattened-image/
---
## Invoering

In deze zelfstudie begeleiden we u bij het converteren van een notitieblok naar een afgeplatte afbeelding in OneNote met behulp van Aspose.Note voor Java. Hierdoor kunt u uw notebook als afbeeldingsbestand opslaan, zodat alle elementen in één afbeeldingsformaat behouden blijven.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

1. Java Development Kit (JDK) op uw systeem geïnstalleerd.
2.  Aspose.Note voor de Java-bibliotheek gedownload en ingesteld in uw Java-project. U kunt de bibliotheek downloaden van[hier](https://releases.aspose.com/note/java/).
3. Basiskennis van Java-programmeren.

## Pakketten importeren

Om te beginnen moet u de benodigde pakketten uit Aspose importeren. Opmerking voor Java:

```java
import java.io.IOException;
import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Stap 1: Documentmap instellen

Definieer eerst de map waarin uw notebookbestand zich bevindt:

```java
String dataDir = "Your Document Directory";
```

 Vervangen`"Your Document Directory"` met het pad naar uw notebookbestand.

## Stap 2: Notebook laden

 Laad vervolgens het notebookbestand met behulp van de`Notebook` klas:

```java
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

 Zorg ervoor dat u deze vervangt`"test.onetoc2"` met de naam van uw notebookbestand.

## Stap 3: Stel de opties voor het opslaan van afbeeldingen in

Stel nu de opties in voor het opslaan van het notebook als afbeelding. We specificeren het opslagformaat als PNG en stellen de resolutie in op 400 DPI:

```java
NotebookImageSaveOptions saveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
ImageSaveOptions documentSaveOptions = saveOptions.getDocumentSaveOptions();
documentSaveOptions.setResolution(400);
```

U kunt de resolutie aanpassen aan uw wensen.

## Stap 4: Maak het notitieboekje plat

Om ervoor te zorgen dat alle elementen in één afbeelding worden afgevlakt, stelt u de`flatten` optie om`true`:

```java
saveOptions.setFlatten(true);
```

Dit zorgt ervoor dat de resulterende afbeelding de lay-out van uw notebook behoudt.

## Stap 5: Afbeelding opslaan

Sla ten slotte het notitieboekje op als een afgeplatte afbeelding:

```java
notebook.save(dataDir + "ExportImageasFlattenedNotebook_out.png", saveOptions);
```

 Vervangen`"ExportImageasFlattenedNotebook_out.png"` met de gewenste uitvoerbestandsnaam.

## Conclusie

Kortom, met Aspose.Note voor Java kunt u uw notitieboekje eenvoudig converteren naar een afgeplatte afbeelding in OneNote. Dit proces zorgt ervoor dat alle elementen in één beeldformaat bewaard blijven, waardoor delen en bekijken eenvoudig wordt.

## Veelgestelde vragen

### Vraag 1: Kan ik de resolutie van het uitvoerbeeld aanpassen?

 A1: Ja, u kunt de resolutie aanpassen aan uw wensen door de`setResolution` methodeparameter.

### V2: Ondersteunt Aspose.Note andere afbeeldingsformaten voor export?

A2: Ja, Aspose.Note ondersteunt verschillende afbeeldingsformaten zoals PNG, JPEG, BMP, enz., voor het exporteren van notebooks.

### Vraag 3: Kan ik de uitvoerafbeelding verder aanpassen?

A3: Ja, Aspose.Note biedt uitgebreide opties voor het aanpassen van de uitvoerafbeelding, inclusief paginaformaat, richting en kwaliteitsinstellingen.

### V4: Is er een proefversie beschikbaar voor Aspose.Note voor Java?

 A4: Ja, u kunt een gratis proefversie verkrijgen via[hier](https://releases.aspose.com/).

### V5: Waar kan ik ondersteuning vinden voor Aspose.Note voor Java?

 A5: U kunt ondersteuning en bronnen vinden op het Aspose.Note-forum[hier](https://forum.aspose.com/c/note/28).