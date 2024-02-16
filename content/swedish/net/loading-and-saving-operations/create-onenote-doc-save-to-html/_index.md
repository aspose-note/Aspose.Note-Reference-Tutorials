---
title: Skapa OneNote-dokument och spara till HTML i Aspose.Note
linktitle: Skapa OneNote-dokument och spara till HTML i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du skapar och sparar Microsoft OneNote-dokument i HTML-format i .NET-applikationer med Aspose.Note API. Följ vår omfattande handledning med steg-för-steg-exempel.
type: docs
weight: 14
url: /sv/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Introduktion

Aspose.Note för .NET är ett kraftfullt API som låter utvecklare arbeta med Microsoft OneNote-dokument programmatiskt i sina .NET-applikationer. Med Aspose.Note kan du skapa, manipulera och konvertera OneNote-filer utan ansträngning. I den här handledningen kommer vi att utforska hur man skapar ett OneNote-dokument och sparar det i HTML-format med hjälp av olika alternativ som tillhandahålls av Aspose.Note för .NET API.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

- Grundläggande kunskaper i programmeringsspråket C#.
- Visual Studio installerat på ditt system.
-  Aspose.Note för .NET API installerat i ditt projekt. Du kan ladda ner den från[här](https://releases.aspose.com/note/net/).
- Kännedom om strukturen i Microsoft OneNote-dokument.

## Importera namnområden

Innan vi dyker in i kodningsdelen, låt oss importera de nödvändiga namnrymden:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Låt oss nu dela upp varje exempel i flera steg och se hur man skapar ett OneNote-dokument och sparar det i HTML-format med Aspose.Note för .NET.

## Steg 1: Skapa ett OneNote-dokument med standardalternativ

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Initiera OneNote-dokument
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Standardformat för all text i dokumentet.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Spara i HTML-format
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

I det här steget initierar vi ett nytt OneNote-dokument, lägger till en sida med en titel och sparar den i HTML-format med standardalternativ.

## Steg 2: Skapa och spara ett specifikt sidintervall till HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Initiera OneNote-dokument
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Standardformat för all text i dokumentet.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Spara i HTML-format
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Här visar vi hur man skapar ett dokument och sparar ett specifikt sidintervall i HTML-format.

## Steg 3: Spara som HTML till Memory Stream med inbäddade resurser

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Ladda OneNote-dokumentet
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Ange HTML-sparalternativ
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Spara dokumentet i en minnesström
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Det här steget illustrerar hur du sparar ett OneNote-dokument i HTML-format med inbäddade resurser (CSS, teckensnitt och bilder) i en minnesström.

## Steg 4: Spara som HTML till fil med resurser i separata filer

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Ladda OneNote-dokumentet
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Ange HTML-sparalternativ
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Spara dokumentet till HTML-fil med resurser lagrade i separata filer
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

I det här steget sparar vi ett OneNote-dokument i HTML-format med alla resurser (CSS, teckensnitt och bilder) lagrade i separata filer.

## Steg 5: Spara som HTML till minnesström med återuppringningar för att spara resurser

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Ange konfigurationen för att spara återuppringningar
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Ange HTML-sparalternativ
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Ladda OneNote-dokumentet
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Spara dokumentet i HTML-format med resurser som hanteras av användardefinierade callbacks
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Lägg till data manuellt i CSS-strömmen
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Här visar vi hur man sparar ett OneNote-dokument i HTML-format med resurser som hanteras av användardefinierade återuppringningar.

## Slutsats

I den här artikeln har vi utforskat hur man arbetar med OneNote-dokument och sparar dem i HTML-format med Aspose.Note för .NET. Genom att följa steg-för-steg-guiden kan du enkelt

 integrera den här funktionen i dina .NET-applikationer, så att du kan manipulera OneNote-filer effektivt.

## FAQ's

### F1: Kan jag anpassa utseendet på den sparade HTML-filen?

S1: Ja, du kan anpassa utseendet genom att ändra CSS-stilmallarna som genereras under konverteringsprocessen.

### F2: Stöder Aspose.Note konvertering till andra format än HTML?

S2: Ja, Aspose.Note stöder konvertering till olika format som PDF, bilder och Microsoft Word-dokument.

### F3: Är Aspose.Note kompatibel med .NET Core-applikationer?

S3: Ja, Aspose.Note är kompatibel med både .NET Framework och .NET Core-applikationer.

### F4: Kan jag extrahera text och bilder från OneNote-dokument med Aspose.Note?

S4: Ja, du kan extrahera text och bilder samt utföra olika andra manipulationer med Aspose.Note API.

### F5: Finns det en testversion tillgänglig för att testa Aspose.Note-funktioner?

 A5: Ja, du kan ladda ner en gratis testversion från[här](https://releases.aspose.com/).