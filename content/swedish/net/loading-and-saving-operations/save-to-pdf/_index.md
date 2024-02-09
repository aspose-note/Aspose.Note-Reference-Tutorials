---
title: Spara till PDF i Aspose.Note
linktitle: Spara till PDF i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du sparar Microsoft OneNote-dokument i PDF-format med Aspose.Note för .NET. Steg-för-steg handledning med kodexempel för sidlayouter i Letter och A4.
type: docs
weight: 26
url: /sv/net/loading-and-saving-operations/save-to-pdf/
---
## Introduktion

I den här handledningen kommer vi att utforska hur man sparar dokument i PDF-format med Aspose.Note för .NET. Aspose.Note är ett kraftfullt bibliotek som gör det möjligt för utvecklare att arbeta med Microsoft OneNote-filer programmatiskt. Vi kommer att täcka förutsättningarna, importera namnutrymmen och tillhandahålla steg-för-steg-guider för att spara dokument till PDF i olika sidlayouter.

## Förutsättningar

Innan vi börjar, se till att du har följande:

- Visual Studio installerat på ditt system.
-  Aspose.Note för .NET-biblioteket har laddats ner och installerats. Du kan ladda ner den från[här](https://releases.aspose.com/note/net/).
- Grundläggande kunskaper i programmeringsspråket C#.

## Importera namnområden

Låt oss först importera de nödvändiga namnrymden till vår C#-kod:

```csharp
using System;
using System.IO;

using Aspose.Note.Saving;
```

Nu när vi har täckta förutsättningarna och namnrymden importerade, låt oss fortsätta med att spara dokument till PDF i olika sidlayouter.

## Steg 1: Spara till PDF med hjälp av Letter Page Settings


```csharp
public static void SaveToPdfUsingLetterPageSettings()
{
    // Sökvägen till dokumentkatalogen.
    string dataDir = "Your Document Directory";

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingLetterPageSettings.pdf");

    //Spara dokumentet.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.Letter });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Förklaring:

- Vi laddar OneNote-dokumentet i Aspose.Note.
- Definiera destinationssökvägen för den sparade PDF-filen.
-  Spara dokumentet till PDF med`PdfSaveOptions` med`PageSettings` satt till`Letter`.

## Steg 2: Spara till PDF med A4-sidinställningar utan höjdbegränsning

```csharp
public static void SaveToPdfUsingA4PageSettingsWithoutHeightLimit()
{
    // Sökvägen till dokumentkatalogen.
    string dataDir = "Your Document Directory";

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(dataDir + "OneNote.one");

    var dst = Path.Combine(dataDir, "SaveToPdfUsingA4PageSettingsWithoutHeightLimit.pdf");

    //Spara dokumentet.
    oneFile.Save(dst, new PdfSaveOptions() { PageSettings = PageSettings.A4NoHeightLimit });

    Console.WriteLine("\nOneNote document saved successfully.\nFile saved at " + dst);
}
```

### Förklaring:

- I likhet med föregående steg laddar vi OneNote-dokumentet i Aspose.Note.
- Definiera destinationssökvägen för den sparade PDF-filen.
-  Spara dokumentet till PDF med`PdfSaveOptions` med`PageSettings` satt till`A4NoHeightLimit`.

## Slutsats

I den här handledningen lärde vi oss hur man sparar dokument i PDF-format med Aspose.Note för .NET. Vi täckte två olika sidlayouter: Letter och A4 utan höjdbegränsning. Med Aspose.Note kan utvecklare enkelt manipulera OneNote-filer programmatiskt, vilket ger flexibilitet och effektivitet i dokumenthanteringsuppgifter.

## FAQ's

### F1: Kan Aspose.Note hantera komplexa OneNote-filer?

S1: Ja, Aspose.Note stöder olika funktioner och funktioner för att effektivt hantera komplexa OneNote-filer.

### F2: Är Aspose.Note lämplig för kommersiella projekt?

 A2: Absolut, Aspose.Note kan enkelt användas i kommersiella projekt. Du kan köpa en licens[här](https://purchase.aspose.com/buy).

### F3: Erbjuder Aspose.Note en gratis provperiod?

 S3: Ja, du kan utforska Aspose.Note med en gratis provperiod tillgänglig[här](https://releases.aspose.com/).

### F4: Var kan jag hitta dokumentation för Aspose.Note?

 A4: Du kan hitta detaljerad dokumentation[här](https://reference.aspose.com/note/net/).

### F5: Behöver du ytterligare hjälp?

 S5: Ställ gärna några frågor eller sök support på Aspose.Note-forumet[här](https://forum.aspose.com/c/note/28).