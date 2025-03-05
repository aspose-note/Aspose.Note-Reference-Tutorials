---
title: Voeg een tekstknooppunt met tag toe in Aspose.Note
linktitle: Voeg een tekstknooppunt met tag toe in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u tekstknooppunten met tags aan OneNote-documenten kunt toevoegen met Aspose.Note voor .NET.
type: docs
weight: 12
url: /nl/net/tag-management/add-text-node-tag/
---
## Invoering

Aspose.Note voor .NET is een krachtige bibliotheek waarmee ontwikkelaars Microsoft OneNote-bestanden programmatisch kunnen maken, manipuleren en converteren met behulp van het .NET-framework. In deze zelfstudie onderzoeken we hoe u een tekstknooppunt met een tag aan een OneNote-document kunt toevoegen met Aspose.Note voor .NET.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

1. Visual Studio: Zorg ervoor dat Visual Studio op uw systeem is geïnstalleerd.
2.  Aspose.Note voor .NET: Download en installeer Aspose.Note voor .NET vanaf de[website](https://releases.aspose.com/note/net/).
3. Basiskennis van C#: maak uzelf vertrouwd met de grondbeginselen van de programmeertaal C#.

## Naamruimten importeren

Eerst moet u de benodigde naamruimten importeren om toegang te krijgen tot de klassen en methoden die nodig zijn om met Aspose.Note voor .NET te werken.

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Stap 1: Maak een documentobject

Initialiseer een Document-object om aan de slag te gaan met een OneNote-document.

```csharp
// Het pad naar de documentenmap.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

## Stap 2: Initialiseer pagina- en overzichtsobjecten

Maak pagina- en overzichtsobjecten om de inhoud van het OneNote-document te structureren.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```

## Stap 3: Voeg een tekstknooppunt met tag toe

Maak een RichText-object met de gewenste tekst en stijl en voeg dit vervolgens toe aan het OutlineElement.

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text = new RichText(doc) { Text = "OneNote text.", ParagraphStyle = textStyle };
text.Tags.Add(NoteTag.CreateYellowStar());
outlineElem.AppendChildLast(text);
```

## Stap 4: Voeg overzichtselement en paginaknooppunten toe

Voeg het OutlineElement toe aan de omtrek en voeg vervolgens de omtrek toe aan de pagina. Voeg ten slotte de pagina toe aan het document.

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Stap 5: Sla het document op

Sla het gewijzigde OneNote-document op een opgegeven locatie op.

```csharp
string dataDir = "Your Document Directory";
string outputPath = Path.Combine(dataDir, "AddTextNodeWithTag_out.one");
doc.Save(outputPath);
```

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u een tekstknooppunt met een tag aan een OneNote-document kunt toevoegen met Aspose.Note voor .NET. Met deze kennis kunt u uw OneNote-bestanden nu programmatisch aanpassen en verbeteren.

## Veelgestelde vragen

### V1: Kan ik meerdere tekstknooppunten met verschillende tags in hetzelfde document toevoegen?

A1: Ja, u kunt meerdere tekstknooppunten met verschillende tags toevoegen door voor elk knooppunt hetzelfde proces te volgen.

### V2: Is Aspose.Note voor .NET compatibel met alle versies van OneNote?

A2: Aspose.Note voor .NET ondersteunt verschillende versies van OneNote, waaronder 2010, 2013, 2016 en hoger.

### Vraag 3: Kan ik de kleuren en stijlen van de tags aanpassen?

A3: Ja, u kunt de tagkleuren en -stijlen aanpassen aan uw wensen.

### V4: Ondersteunt Aspose.Note voor .NET documentversleuteling?

A4: Ja, Aspose.Note voor .NET ondersteunt documentversleuteling om gegevensbeveiliging te garanderen.

### V5: Waar kan ik meer bronnen en ondersteuning vinden voor Aspose.Note voor .NET?

 A5: U kunt de verkennen[Aspose.Note voor .NET-documentatie](https://reference.aspose.com/note/net/)en hulp zoeken bij de[Aspose.Note-forum](https://forum.aspose.com/c/note/28).