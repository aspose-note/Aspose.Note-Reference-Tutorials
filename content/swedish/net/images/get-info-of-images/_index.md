---
title: Få information om bilder i Aspose.Note
linktitle: Få information om bilder i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du extraherar bildinformation från Microsoft OneNote-filer med Aspose.Note för .NET. Följ vår steg-för-steg-guide för effektiv utveckling.
type: docs
weight: 13
url: /sv/net/images/get-info-of-images/
---
## Introduktion

I en värld av .NET-utveckling erbjuder Aspose.Note en kraftfull uppsättning verktyg för att arbeta med Microsoft OneNote-filer. En vanlig uppgift som utvecklare ofta möter är att extrahera information från bilder inbäddade i dessa anteckningar. Oavsett om det gäller att erhålla dimensioner, filnamn eller ändringstider, förenklar Aspose.Note denna process.

## Förutsättningar

Innan vi dyker in i att extrahera bildinformation med Aspose.Note, se till att du har följande:

1. Grundläggande kunskaper i C#: Förtrogenhet med programmeringsspråket C# är avgörande för att förstå kodexemplen.
2.  Aspose.Note för .NET installerat: Se till att du har Aspose.Note-biblioteket installerat i din utvecklingsmiljö. Du kan ladda ner den[här](https://releases.aspose.com/note/net/).

## Importera namnområden

Innan vi börjar, låt oss importera de nödvändiga namnrymden:

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System;
```

## Steg 1: Ladda dokumentet

Ladda först in mål OneNote-dokumentet i Aspose.Note:

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";

// Ladda dokumentet i Aspose.Note.
Document oneFile = new Document(dataDir + "Aspose.one");
```

 Byta ut`"Your Document Directory"` med sökvägen till din OneNote-fil.

## Steg 2: Hämta bildinformation

Hämta sedan alla bildnoder från dokumentet:

```csharp
// Hämta alla bildnoder
IList<Aspose.Note.Image> images = oneFile.GetChildNodes<Aspose.Note.Image>();
```

Det här kodavsnittet hämtar alla bildnoder i det inlästa OneNote-dokumentet.

## Steg 3: Iterera genom bilder

Låt oss nu iterera genom varje bildnod för att extrahera dess metadata:

```csharp
foreach (Aspose.Note.Image image in images)
{
    Console.WriteLine("Width: {0}", image.Width);
    Console.WriteLine("Height: {0}", image.Height);
    Console.WriteLine("OriginalWidth: {0}", image.OriginalWidth);
    Console.WriteLine("OriginalHeight: {0}", image.OriginalHeight);
    Console.WriteLine("FileName: {0}", image.FileName);
    Console.WriteLine("LastModifiedTime: {0}", image.LastModifiedTime);
    Console.WriteLine();
}
```

Denna loop skriver ut olika attribut för varje bild, såsom bredd, höjd, originalmått, filnamn och senast ändrad tid.

## Slutsats

Med Aspose.Note för .NET blir det en sömlös process att extrahera bildinformation från OneNote-dokument. Genom att följa stegen som beskrivs i den här handledningen kan utvecklare effektivt hämta metadata från inbäddade bilder, vilket ger dem möjlighet att bygga robusta applikationer.

## FAQ's

### F1: Är Aspose.Note kompatibel med alla versioner av Microsoft OneNote?

S1: Aspose.Note stöder olika format av OneNote-filer, inklusive .one, .onepkg och .onetoc2, vilket säkerställer kompatibilitet mellan olika versioner.

### F2: Kan jag ändra bildens egenskaper med Aspose.Note?

S2: Ja, Aspose.Note låter dig manipulera bildegenskaper såsom dimensioner, filnamn och modifieringstider programmatiskt.

### F3: Erbjuder Aspose.Note stöd för .NET Core?

S3: Ja, Aspose.Note ger stöd för .NET Core, vilket möjliggör plattformsoberoende utveckling för dina applikationer.

### F4: Finns det en gratis testversion tillgänglig för Aspose.Note?

S4: Ja, du kan få tillgång till en gratis testversion av Aspose.Note för att utforska dess funktioner innan du gör ett köp.

### F5: Var kan jag hitta ytterligare support eller hjälp med Aspose.Note?

 S5: För eventuella frågor eller hjälp kan du besöka Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28).