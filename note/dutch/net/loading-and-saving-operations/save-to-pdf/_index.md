---
title: Opslaan als PDF in Aspose.Note
linktitle: Opslaan als PDF in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u Microsoft OneNote-documenten in PDF-indeling kunt opslaan met Aspose.Note voor .NET. Stapsgewijze zelfstudie met codevoorbeelden voor Letter- en A4-paginalay-outs.
weight: 26
url: /nl/net/loading-and-saving-operations/save-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan als PDF in Aspose.Note

## Invoering

In deze zelfstudie onderzoeken we hoe u documenten in PDF-indeling kunt opslaan met Aspose.Note voor .NET. Aspose.Note is een krachtige bibliotheek waarmee ontwikkelaars programmatisch met Microsoft OneNote-bestanden kunnen werken. We bespreken de vereisten, importeren naamruimten en bieden stapsgewijze handleidingen voor het opslaan van documenten in PDF in verschillende paginalay-outs.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

- Visual Studio is op uw systeem geïnstalleerd.
-  Aspose.Note voor .NET-bibliotheek gedownload en geïnstalleerd. Je kunt het downloaden van[hier](https://releases.aspose.com/note/net/).
- Basiskennis van de programmeertaal C#.

## Naamruimten importeren

Laten we eerst de benodigde naamruimten in onze C#-code importeren:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Nu we aan de vereisten hebben voldaan en de naamruimten hebben geïmporteerd, gaan we verder met het opslaan van documenten in PDF in verschillende paginalay-outs.

## Stap 1: Opslaan naar PDF met behulp van Letter-pagina-instellingen


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Het pad naar de documentenmap.
    string dataDir = "Your Document Directory";

    // Laad het document in Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    // Bewaar het document.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Uitleg:

- We laden het OneNote-document in Aspose.Note.
- Definieer het bestemmingspad voor het opgeslagen PDF-bestand.
-  Sla het document op in PDF met behulp van`PdfSaveOptions` met`PageSettings` ingesteld op`Letter`.

## Stap 2: Opslaan naar PDF met A4-pagina-instellingen zonder hoogtelimiet

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Het pad naar de documentenmap.
    string dataDir = "Your Document Directory";

    // Laad het document in Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    // Bewaar het document.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Uitleg:

- Net als bij de vorige stap laden we het OneNote-document in Aspose.Note.
- Definieer het bestemmingspad voor het opgeslagen PDF-bestand.
-  Sla het document op in PDF met behulp van`PdfSaveOptions` met`PageSettings` ingesteld op`A4NoHeightLimit`.

## Conclusie

In deze zelfstudie hebben we geleerd hoe u documenten in PDF-indeling kunt opslaan met Aspose.Note voor .NET. We hebben twee verschillende pagina-indelingen besproken: Letter en A4 zonder hoogtelimiet. Met Aspose.Note kunnen ontwikkelaars OneNote-bestanden eenvoudig programmatisch manipuleren, wat flexibiliteit en efficiëntie biedt bij documentbeheertaken.

## Veelgestelde vragen

### V1: Kan Aspose.Note omgaan met complexe OneNote-bestanden?

A1: Ja, Aspose.Note ondersteunt verschillende functies en functionaliteiten om complexe OneNote-bestanden effectief te verwerken.

### Vraag 2: Is Aspose.Note geschikt voor commerciële projecten?

 A2: Absoluut, Aspose.Note kan gemakkelijk in commerciële projecten worden gebruikt. U kunt een licentie kopen[hier](https://purchase.aspose.com/buy).

### V3: Biedt Aspose.Note een gratis proefperiode?

 A3: Ja, u kunt Aspose.Note verkennen met een gratis proefversie[hier](https://releases.aspose.com/).

### V4: Waar kan ik documentatie voor Aspose.Note vinden?

 A4: U kunt gedetailleerde documentatie vinden[hier](https://reference.aspose.com/note/net/).

### Vraag 5: Heeft u verdere hulp nodig?

 A5: Stel gerust vragen of zoek ondersteuning op het Aspose.Note-forum[hier](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
