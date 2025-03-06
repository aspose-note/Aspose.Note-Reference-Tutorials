---
title: Öppna och stäng projekt med taggar i Aspose.Note
linktitle: Öppna och stäng projekt med taggar i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du manipulerar Microsoft OneNote-filer programmatiskt med Aspose.Note för .NET. Öppna och stäng projekt med taggar effektivt.
weight: 15
url: /sv/net/tag-management/open-close-projects-tags/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Öppna och stäng projekt med taggar i Aspose.Note

## Introduktion

den här handledningen kommer vi att lära oss hur man använder Aspose.Note för .NET för att öppna och stänga projekt med taggar. Aspose.Note är ett kraftfullt API som tillåter utvecklare att arbeta med Microsoft OneNote-filer programmatiskt, vilket möjliggör uppgifter som att manipulera text, bilder och taggar i dokumenten.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

## Importera namnområden

```csharp
using System.IO;
using System.Linq;
```

Låt oss nu dela upp varje exempel i flera steg:

## Steg 1: Ladda dokumentet

Först måste vi ladda dokumentet i Aspose.Note.

```csharp
string dataDir = "Your Document Directory";
var oneFile = new Document(Path.Combine(dataDir, "ProjectNotes.one"));
```

## Steg 2: Stäng Project C-objekt

Låt oss nu stänga alla kryssrutor relaterade till 'Projekt C'.

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

## Steg 3: Spara de stängda projekt C-anteckningarna

Spara det ändrade dokumentet med stängda 'Project C'-objekt.

```csharp
oneFile.Save("Path to save the closed Project C notes");
```

## Steg 4: Öppna Project C-objekt

Låt oss sedan öppna alla kryssrutor relaterade till 'Projekt C'.

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

## Steg 5: Spara Open Project C Notes

Spara det ändrade dokumentet med öppnade "Project C"-objekt.

```csharp
oneFile.Save(Path.Combine(dataDir, "ProjectNoteWithOpenProjectC.one"));
```

Nu har du lärt dig hur du öppnar och stänger projekt med taggar i Aspose.Note med .NET.

## Slutsats

Aspose.Note för .NET ger ett bekvämt sätt att manipulera OneNote-dokument programmatiskt. Genom att följa denna handledning kan du effektivt hantera dina projekt genom att öppna och stänga objekt med taggar.

## FAQ's

### F1: Är Aspose.Note kompatibel med alla versioner av OneNote?

S1: Aspose.Note stöder Microsoft OneNote 2010 och nyare versioner.

### F2: Kan jag använda Aspose.Note för kommersiella projekt?

 S2: Ja, du kan använda Aspose.Note för både personliga och kommersiella projekt. Besök[här](https://purchase.aspose.com/buy) att köpa en licens.

### F3: Erbjuder Aspose.Note en gratis provperiod?

 A3: Ja, du kan få en gratis provperiod[här](https://releases.aspose.com/).

### F4: Var kan jag hitta dokumentation för Aspose.Note?

 S4: Du kan hitta dokumentationen[här](https://reference.aspose.com/note/net/).

### F5: Var kan jag få support för Aspose.Note?

 S5: För support kan du besöka Aspose.Note[forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
