---
title: Voeg een tabelknooppunt met tag toe in Aspose.Note
linktitle: Voeg een tabelknooppunt met tag toe in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u tabellen met tags toevoegt in Aspose.Note voor .NET. Verbeter uw vaardigheden op het gebied van documentmanipulatie programmatisch.
type: docs
weight: 11
url: /nl/net/tag-management/add-table-node-tag/
---
## Invoering

In deze zelfstudie begeleiden we u bij het toevoegen van een tabelknooppunt met een tag met behulp van Aspose.Note voor .NET. Volg de onderstaande stappen om dit te bereiken.

## Naamruimten importeren

Zorg ervoor dat u, voordat u aan de slag gaat, de benodigde naamruimten importeert om met Aspose te kunnen werken. Opmerking:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Vereisten

Zorg ervoor dat u aan de volgende vereisten voldoet voordat u doorgaat:

1.  Installatie: Download en installeer de Aspose.Note voor .NET-bibliotheek van[hier](https://releases.aspose.com/note/net/).
2.  Licentie: Verkrijg een licentie of gebruik een[tijdelijke licentie](https://purchase.aspose.com/temporary-license/) om de bibliotheek te gebruiken.
3. Ontwikkelomgeving: Zorg dat er een compatibele ontwikkelomgeving is opgezet, zoals Visual Studio.

## Stap 1: Initialiseer document- en pagina-objecten

 Begin met het maken van een exemplaar van het`Document` klasse en het initialiseren van a`Page` voorwerp:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Stap 2: Maak tabel-, rij- en celobjecten

 Initialiseer de`Table`, `TableRow` , En`TableCell` voorwerpen:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Stap 3: Voeg inhoud in cel in

 Voeg inhoud aan de cel toe met behulp van de`AppendChildLast` methode:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Stap 4: Initialiseer het tabelknooppunt

 Initialiseer de`Table` object met gespecificeerde eigenschappen:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Stap 5: Rij toevoegen aan tabel

Voeg het rijknooppunt toe aan de tabel:

```csharp
table.AppendChildLast(row);
```

## Stap 6: Tag toevoegen aan tabelknooppunt

Voeg een tag toe voor het tabelknooppunt:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Stap 7: Voeg een tabelknooppunt toe aan het overzichtselement

 Creëer een`Outline` En`OutlineElement` om het tabelknooppunt toe te voegen:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Stap 8: Document opslaan

Sla het OneNote-document op:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Nadat u deze stappen hebt gevolgd, zou u met succes een tabelknooppunt met een tag moeten hebben toegevoegd met behulp van Aspose.Note voor .NET.

## Conclusie

In deze zelfstudie hebben we het proces besproken van het toevoegen van een tabelknooppunt met een tag in Aspose.Note voor .NET. Door deze stappen te volgen, kunt u OneNote-documenten efficiënt programmatisch manipuleren, waardoor uw mogelijkheden voor documentbeheer worden verbeterd.

## Veelgestelde vragen

### Vraag 1: Is Aspose.Note compatibel met alle versies van .NET?

A1: Aspose.Note voor .NET ondersteunt .NET Framework versies 2.0 en hoger, inclusief .NET Core en .NET Standard.

### V2: Kan ik Aspose.Note uitproberen voordat ik een licentie aanschaf?

 A2: Ja, u kunt een gratis proefversie van Aspose.Note verkrijgen[hier](https://releases.aspose.com/).

### V3: Hoe verkrijg ik een tijdelijke licentie voor Aspose.Note?

 A3: U kunt een tijdelijke licentie krijgen van[deze link](https://purchase.aspose.com/temporary-license/), die 30 dagen geldig is.

### V4: Ondersteunt Aspose.Note documentversleuteling?

A4: Ja, Aspose.Note biedt ondersteuning voor het coderen van OneNote-documenten om gegevensbeveiliging te garanderen.

### V5: Is er technische ondersteuning beschikbaar voor Aspose.Note-gebruikers?

 A5: Ja, technische ondersteuning wordt geboden via de Aspose-forums[hier](https://forum.aspose.com/c/note/28), waar u hulp kunt inroepen van deskundigen.