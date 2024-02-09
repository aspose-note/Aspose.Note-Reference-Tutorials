---
title: Konvertera anteckningsböcker till bild (tillplattad) i Aspose Note .NET
linktitle: Konvertera anteckningsböcker till bild (tillplattad) i Aspose Note .NET
second_title: Aspose.Note .NET API
description: Lär dig hur du konverterar OneNote-anteckningsböcker till tillplattade bilder med Aspose.Note för .NET. Steg-för-steg-guide för sömlös integration.
type: docs
weight: 12
url: /sv/net/notebook-operations/convert-to-image-flattened/
---
## Introduktion

I den här handledningen kommer vi att lära oss hur du använder Aspose.Note för .NET för att konvertera anteckningsböcker till tillplattade bilder. Vi delar upp processen i enkla steg för att hjälpa dig förstå och implementera den effektivt.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1.  Aspose.Note for .NET: Om du inte redan har gjort det, ladda ner och installera Aspose.Note for .NET från[här](https://releases.aspose.com/note/net/).
2. Utvecklingsmiljö: Se till att du har en lämplig utvecklingsmiljö inrättad för .NET-utveckling.
3. OneNote Notebook: Förbered OneNote-anteckningsboken som du vill konvertera till en bild.

## Importera namnområden

Innan du börjar med konverteringsprocessen måste du importera de nödvändiga namnrymden i din kod:

```csharp
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Låt oss nu dyka in i steg-för-steg-guiden för att konvertera anteckningsböcker till tillplattade bilder med Aspose.Note för .NET.

## Steg 1: Ladda anteckningsboken

Ladda först OneNote-anteckningsboken som du vill konvertera till din applikation.

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";

// Ladda en OneNote-anteckningsbok
var notebook = new Notebook(dataDir + "Notizbuch öffnen.onetoc2");
```

## Steg 2: Ställ in sparalternativ

Definiera sparalternativen för anteckningsboken, inklusive bildformat och upplösning.

```csharp
var notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);
var documentSaveOptions = notebookSaveOptions.DocumentSaveOptions;

documentSaveOptions.Resolution = 400;
notebookSaveOptions.Flatten = true;
```

## Steg 3: Spara anteckningsboken som bild

Spara nu anteckningsboken som en tillplattad bild med de definierade sparalternativen.

```csharp
dataDir = dataDir + "ConvertToImageAsFlattenedNotebook_out.png";

// Spara anteckningsboken
notebook.Save(dataDir, notebookSaveOptions);
```

## Slutsats

I den här handledningen har vi lärt oss hur man konverterar anteckningsböcker till tillplattade bilder med Aspose.Note för .NET. Genom att följa steg-för-steg-guiden kan du sömlöst integrera denna funktion i dina .NET-applikationer.

## FAQ's

### F1: Kan Aspose.Note för .NET hantera komplexa bärbara datorer?

S1: Ja, Aspose.Note för .NET kan hantera komplexa bärbara datorer effektivt.

### F2: Finns det en gratis testversion tillgänglig för Aspose.Note för .NET?

 A2: Ja, du kan ladda ner en gratis testversion från[här](https://releases.aspose.com/).

### F3: Ger Aspose support för sina produkter?

 S3: Ja, du kan få stöd från Aspose-communityt[här](https://forum.aspose.com/c/note/28).

### F4: Kan jag köpa en tillfällig licens för Aspose.Note för .NET?

 S4: Ja, du kan köpa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag hitta dokumentation för Aspose.Note för .NET?

 S5: Du kan hitta dokumentationen[här](https://reference.aspose.com/note/net/).