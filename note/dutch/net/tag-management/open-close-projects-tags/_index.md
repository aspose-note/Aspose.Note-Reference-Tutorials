---
title: Open en sluit projecten met tags in Aspose.Note
linktitle: Open en sluit projecten met tags in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u Microsoft OneNote-bestanden programmatisch kunt manipuleren met Aspose.Note voor .NET. Open en sluit projecten efficiënt met tags.
weight: 15
url: /nl/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Open en sluit projecten met tags in Aspose.Note

## Invoering

In deze zelfstudie leren we hoe u Aspose.Note voor .NET kunt gebruiken om projecten met tags te openen en te sluiten. Aspose.Note is een krachtige API waarmee ontwikkelaars programmatisch met Microsoft OneNote-bestanden kunnen werken, waardoor taken mogelijk worden zoals het manipuleren van tekst, afbeeldingen en tags in de documenten.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

## Naamruimten importeren

```csharp
using System.IO;
using System.Linq;
```

Laten we nu elk voorbeeld in meerdere stappen opsplitsen:

## Stap 1: Laad het document

Eerst moeten we het document in Aspose.Note laden.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Stap 2: Sluit Project C-items

Laten we nu alle selectievakjes sluiten die betrekking hebben op 'Project C'.

```csharp
foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && !checkBox.Checked)
        {
            checkBox.SetCompleted();
        }
    }
}
```

## Stap 3: Bewaar de gesloten Project C-notities

Sla het gewijzigde document op met gesloten 'Project C'-items.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Stap 4: Open Project C-items

Laten we vervolgens alle selectievakjes openen die betrekking hebben op 'Project C'.

```csharp
var oneFile = new Document("Path to the closed Project C notes");

foreach (var node in oneFile.GetChildNodes<ITaggable>())
{
    foreach (var checkBox in node.Tags.OfType<CheckBox>())
    {
        if (checkBox.Label.Contains("Project C") && checkBox.Checked)
        {
            checkBox.SetOpen();
        }
    }
}
```

## Stap 5: Bewaar de Open Project C-notities

Sla het gewijzigde document op met geopende 'Project C'-items.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Nu heb je geleerd hoe je projecten met tags in Aspose.Note kunt openen en sluiten met behulp van .NET.

## Conclusie

Aspose.Note voor .NET biedt een handige manier om OneNote-documenten programmatisch te manipuleren. Door deze tutorial te volgen, kunt u uw projecten efficiënt beheren door items te openen en te sluiten met behulp van tags.

## Veelgestelde vragen

### V1: Is Aspose.Note compatibel met alle versies van OneNote?

A1: Aspose.Note ondersteunt Microsoft OneNote 2010 en nieuwere versies.

### V2: Kan ik Aspose.Note gebruiken voor commerciële projecten?

 A2: Ja, u kunt Aspose.Note gebruiken voor zowel persoonlijke als commerciële projecten. Bezoek[hier](https://purchase.aspose.com/buy) om een licentie aan te schaffen.

### V3: Biedt Aspose.Note een gratis proefperiode?

 A3: Ja, u kunt een gratis proefperiode krijgen[hier](https://releases.aspose.com/).

### V4: Waar kan ik documentatie voor Aspose.Note vinden?

 A4: U kunt de documentatie vinden[hier](https://reference.aspose.com/note/net/).

### V5: Waar kan ik ondersteuning krijgen voor Aspose.Note?

 A5: Voor ondersteuning kunt u terecht op Aspose.Note[forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
