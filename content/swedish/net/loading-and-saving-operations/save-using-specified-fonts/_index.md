---
title: Spara med angivna teckensnitt i Aspose.Note
linktitle: Spara med angivna teckensnitt i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du sparar dokument med specificerade typsnitt i Aspose.Note för .NET. Anpassa teckensnittsinställningar enkelt för konsekvent dokumentformatering.
type: docs
weight: 28
url: /sv/net/loading-and-saving-operations/save-using-specified-fonts/
---
## Introduktion

I den här handledningen kommer vi att lära oss hur du sparar dokument med angivna typsnitt i Aspose.Note för .NET. Vi kommer att utforska olika metoder för att uppnå detta, steg för steg.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1.  Aspose.Note for .NET: Se till att du har installerat Aspose.Note for .NET. Du kan ladda ner den från[här](https://releases.aspose.com/note/net/).

2. Utvecklingsmiljö: Du behöver en utvecklingsmiljö inrättad för .NET-utveckling.

## Importera namnområden

Låt oss först importera de nödvändiga namnrymden:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Steg 1: Spara med standardteckensnittsnamn

I det här steget sparar vi ett dokument med ett angivet standardtypsnittsnamn.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Sökvägen till dokumentkatalogen.
    string dataDir = "Your Document Directory";

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Spara dokumentet som PDF med angivet standardteckensnitt.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Steg 2: Spara med standardteckensnitt från fil

Låt oss sedan spara ett dokument med ett standardteckensnitt som laddas från en fil.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Sökvägen till dokumentkatalogen.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Spara dokumentet som PDF med standardteckensnittet laddat från filen.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Steg 3: Spara med standardteckensnitt från Stream

Slutligen, låt oss spara ett dokument med ett standardteckensnitt som laddas från en ström.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Sökvägen till dokumentkatalogen.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Spara dokumentet som PDF med standardteckensnittet laddat från stream.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Slutsats

I den här handledningen undersökte vi hur man sparar dokument med angivna typsnitt i Aspose.Note för .NET. Genom att följa dessa steg kan du anpassa teckensnittsinställningarna efter dina krav, och se till att dina dokument formateras som önskat.

## FAQ's

### F1: Kan jag använda vilket typsnitt som helst för att spara dokument i Aspose.Note?

S1: Ja, du kan ange vilket typsnitt som helst för att spara dokument. Se bara till att teckensnittsfilen är tillgänglig och laddad korrekt.

### F2: Är Aspose.Note kompatibel med olika dokumentformat?

S2: Aspose.Note fungerar främst med OneNote-dokument men ger alternativ för att spara i olika format inklusive PDF.

### F3: Hur kan jag hantera saknade teckensnitt när jag sparar dokument?

S3: Aspose.Note erbjuder alternativ för att använda standardteckensnitt om det angivna teckensnittet saknas, vilket säkerställer konsekvent dokumentformatering.

### F4: Stöder Aspose.Note inbäddning av teckensnitt i utdatadokument?

S4: Ja, Aspose.Note tillåter inbäddning av typsnitt för att säkerställa dokumentportabilitet och konsekvent rendering över olika plattformar.

### F5: Var kan jag få ytterligare hjälp med Aspose.Note?

 S5: För ytterligare hjälp eller teknisk support kan du besöka[Aspose.Note forum](https://forum.aspose.com/c/note/28).