---
title: Maak een document met paginatitel in Aspose.Note
linktitle: Maak een document met paginatitel in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u documenten met titelpagina's maakt met Aspose.Note voor .NET. Volg onze stapsgewijze handleiding voor een naadloze integratie.
weight: 13
url: /nl/net/loading-and-saving-operations/create-doc-with-page-title/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een document met paginatitel in Aspose.Note

## Invoering

In deze zelfstudie begeleiden we u bij het maken van een document met een titelpagina met behulp van Aspose.Note voor .NET. Aspose.Note is een krachtige API waarmee ontwikkelaars programmatisch met Microsoft OneNote-bestanden kunnen werken.

## Vereisten

Voordat we beginnen, zorg ervoor dat u de volgende vereisten hebt geïnstalleerd en ingesteld:

### Visual Studio-installatie

1. Visual Studio downloaden: Download en installeer Visual Studio vanaf de Microsoft-website als u dat nog niet heeft gedaan.

2. Installeer .NET Development Workload: Zorg ervoor dat u tijdens het installatieproces de werklast ".NET desktop development" selecteert om er zeker van te zijn dat u over alle benodigde componenten voor .NET-ontwikkeling beschikt.

3. Maak een nieuw project: Open Visual Studio en maak een nieuw project (consoletoepassing of een ander type van uw voorkeur).

### Aspose.Opmerking installatie

1.  Aspose.Note ophalen: Download de Aspose.Note voor .NET-bibliotheek van de[website](https://releases.aspose.com/note/net/).

2. Aspose.Note installeren via NuGet: Als alternatief kunt u Aspose.Note voor .NET installeren via NuGet Package Manager in Visual Studio. Zoek eenvoudigweg naar "Aspose.Note" en installeer de nieuwste versie.

## Naamruimten importeren

Eerst moet u de benodigde naamruimten importeren om Aspose.Note in uw project te gebruiken.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Laten we nu het proces van het maken van een document met een paginatitel in meerdere stappen opsplitsen:

## Stap 1: Maak een documentobject

```csharp
//Maak een object van de klasse Document
Document doc = new Aspose.Note.Document();
```

## Stap 2: Initialiseer het paginaklasse-object

```csharp
// Initialiseer het Page-klasseobject
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Stap 3: Stel de standaardstijl voor tekst in

```csharp
// Standaardstijl voor alle tekst in het document.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Stap 4: Stel de eigenschappen van de paginatitel in

```csharp
// Paginatiteleigenschappen instellen
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Stap 5: Voeg een paginaknooppunt toe aan het document

```csharp
// Voeg een paginaknooppunt toe aan het document
doc.AppendChildLast(page);
```

## Stap 6: Bewaar OneNote-document

```csharp
// OneNote-document opslaan
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Conclusie

Gefeliciteerd! U hebt met succes een document met een titelpagina gemaakt met Aspose.Note voor .NET. Deze zelfstudie biedt een stapsgewijze handleiding waarmee u Aspose.Note kunt integreren in uw .NET-toepassingen voor het programmatisch beheren van OneNote-bestanden.

## Veelgestelde vragen

### Vraag 1: Kan ik de titeltekststijl aanpassen?

A1: Ja, u kunt de letterkleur, de letternaam en de lettergrootte van de titeltekst aanpassen aan uw wensen.

### Vraag 2: Is Aspose.Note compatibel met .NET Core?

A2: Ja, Aspose.Note ondersteunt .NET Core, waardoor u platformonafhankelijke applicaties kunt ontwikkelen.

### Vraag 3: Kan ik afbeeldingen en bijlagen aan het document toevoegen?

A3: Absoluut! Aspose.Note biedt API's om afbeeldingen, bijlagen en andere elementen naadloos aan uw OneNote-documenten toe te voegen.

### V4: Ondersteunt Aspose.Note het lezen van bestaande OneNote-bestanden?

A4: Ja, u kunt Aspose.Note gebruiken om bestaande OneNote-bestanden eenvoudig te lezen, wijzigen en manipuleren.

### Vraag 5: Waar kan ik ondersteuning vinden als ik problemen tegenkom?

 A5: U kunt ondersteuning en hulp vinden op de[Aspose.Note-forum](https://forum.aspose.com/c/note/28), waar experts en communityleden u kunnen helpen met uw vragen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
