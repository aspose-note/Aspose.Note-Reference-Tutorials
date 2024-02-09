---
title: Skapa dokument med sidrubrik i Aspose.Note
linktitle: Skapa dokument med sidrubrik i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du skapar dokument med titelsidor med Aspose.Note för .NET. Följ vår steg-för-steg-guide för sömlös integration.
type: docs
weight: 13
url: /sv/net/loading-and-saving-operations/create-doc-with-page-title/
---
## Introduktion

I den här handledningen guidar vi dig genom processen att skapa ett dokument med en titelsida med Aspose.Note för .NET. Aspose.Note är ett kraftfullt API som låter utvecklare arbeta med Microsoft OneNote-filer programmatiskt.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar installerade och konfigurerade:

### Installation av Visual Studio

1. Ladda ner Visual Studio: Om du inte redan har gjort det, ladda ner och installera Visual Studio från Microsofts webbplats.

2. Installera .NET Development Workload: Under installationsprocessen, se till att välja ".NET desktop development"-arbetsbelastningen för att säkerställa att du har alla nödvändiga komponenter för .NET-utveckling.

3. Skapa ett nytt projekt: Öppna Visual Studio och skapa ett nytt projekt (konsolapplikation eller någon annan typ du föredrar).

### Aspose.Note Installation

1.  Skaffa Aspose.Note: Ladda ner Aspose.Note för .NET-biblioteket från[hemsida](https://releases.aspose.com/note/net/).

2. Installera Aspose.Note via NuGet: Alternativt kan du installera Aspose.Note för .NET via NuGet Package Manager i Visual Studio. Sök helt enkelt efter "Aspose.Note" och installera den senaste versionen.

## Importera namnområden

Först måste du importera de nödvändiga namnrymden för att använda Aspose.Note i ditt projekt.

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Drawing;
using System.Globalization;
```

Låt oss nu dela upp processen att skapa ett dokument med en sidrubrik i flera steg:

## Steg 1: Skapa ett dokumentobjekt

```csharp
// Skapa ett objekt av klassen Document
Document doc = new Aspose.Note.Document();
```

## Steg 2: Initiera sidklassobjekt

```csharp
// Initiera Sidklassobjekt
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Steg 3: Ställ in standardstil för text

```csharp
// Standardformat för all text i dokumentet.
ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```

## Steg 4: Ställ in egenskaper för sidrubrik

```csharp
// Ställ in sidtitelegenskaper
page.Title = new Title(doc)
{
    TitleText = new RichText(doc) { Text = "Title text.", ParagraphStyle = textStyle },
    TitleDate = new RichText(doc) { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
    TitleTime = new RichText(doc) { Text = "12:34", ParagraphStyle = textStyle }
};
```

## Steg 5: Lägg till sidnod i dokumentet

```csharp
// Lägg till sidnod i dokumentet
doc.AppendChildLast(page);
```

## Steg 6: Spara OneNote-dokument

```csharp
// Spara OneNote-dokument
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithPageTitle_out.one";
doc.Save(dataDir);
```

## Slutsats

Grattis! Du har framgångsrikt skapat ett dokument med en titelsida med Aspose.Note för .NET. Denna handledning gav en steg-för-steg-guide som hjälper dig att integrera Aspose.Note i dina .NET-applikationer för att hantera OneNote-filer programmatiskt.

## FAQ's

### F1: Kan jag anpassa titeltextstilen?

A1: Ja, du kan anpassa teckensnittsfärg, teckensnittsnamn och teckenstorlek för titeltexten enligt dina krav.

### F2: Är Aspose.Note kompatibel med .NET Core?

S2: Ja, Aspose.Note stöder .NET Core, vilket gör att du kan utveckla plattformsoberoende applikationer.

### F3: Kan jag lägga till bilder och bilagor till dokumentet?

A3: Absolut! Aspose.Note tillhandahåller API:er för att lägga till bilder, bilagor och andra element till dina OneNote-dokument sömlöst.

### F4: Stöder Aspose.Note läsning av befintliga OneNote-filer?

S4: Ja, du kan använda Aspose.Note för att enkelt läsa, ändra och manipulera befintliga OneNote-filer.

### F5: Var kan jag hitta support om jag stöter på några problem?

 S5: Du kan hitta stöd och hjälp på[Aspose.Note forum](https://forum.aspose.com/c/note/28), där experter och communitymedlemmar kan hjälpa dig med dina frågor.