---
title: Utforska sidrevisioner i Aspose.Note-dokument
linktitle: Utforska sidrevisioner i Aspose.Note-dokument
second_title: Aspose.Note .NET API
description: Lär dig hur du utforskar sidrevideringar i Aspose.Note-dokument med hjälp av .NET-ramverket med steg-för-steg-vägledning.
type: docs
weight: 14
url: /sv/net/note-manipulation/page-revisions-exploration/
---
## Introduktion

I den här handledningen kommer vi att fördjupa oss i att utforska sidversioner i Aspose.Note-dokument med hjälp av .NET-ramverket. Aspose.Note är ett kraftfullt bibliotek som gör det möjligt för utvecklare att arbeta med Microsoft OneNote-filer programmatiskt, och erbjuder olika funktioner för att manipulera och extrahera data från dessa filer.

## Förutsättningar

Innan vi börjar, se till att du har ställt in följande förutsättningar:

### 1. Ladda ner och installera Aspose.Note för .NET

 Besök[nedladdningssida](https://releases.aspose.com/note/net/) och ladda ner Aspose.Note för .NET-biblioteket. Följ installationsinstruktionerna för att ställa in biblioteket i din utvecklingsmiljö.

### 2. Ladda nödvändiga namnutrymmen

Se till att importera de nödvändiga namnområdena i ditt .NET-projekt för att få åtkomst till Aspose.Note-funktionerna sömlöst.

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

Låt oss nu dela upp processen för att utforska sidrevisioner i steg-för-steg-instruktioner:

## Steg 1: Ladda dokumentet

Först måste vi ladda Aspose.Note-dokumentet, vilket säkerställer att dokumenthistoriken kan laddas.

```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one", new LoadOptions { LoadHistory = true });
```

## Steg 2: Hämta sidrevisionerna

När dokumentet är laddat kan vi hämta revisionerna för en specifik sida. I det här exemplet får vi revisioner för första sidan.

```csharp
Page firstPage = document.FirstChild;
foreach (Page pageRevision in document.GetPageHistory(firstPage))
{
    /*Use pageRevision like a regular page.*/
    Console.WriteLine("LastModifiedTime: {0}", pageRevision.LastModifiedTime);
    Console.WriteLine("CreationTime: {0}", pageRevision.CreationTime);
    Console.WriteLine("Title: {0}", pageRevision.Title);
    Console.WriteLine("Level: {0}", pageRevision.Level);
    Console.WriteLine("Author: {0}", pageRevision.Author);
    Console.WriteLine();
}
```

## Steg 3: Iterera genom revisioner

Inom slingan, iterera genom varje version av sidan och få tillgång till dess egenskaper som senast ändrad tid, skapelsetid, titel, nivå och författare.

## Slutsats

Att utforska sidversioner i Aspose.Note-dokument med .NET är en enkel process. Genom att följa stegen som beskrivs i denna handledning kan du effektivt hämta och analysera revisionshistoriken för dina OneNote-filer programmatiskt.

## FAQ's

### F1: Kan jag använda Aspose.Note för .NET för att skapa nya OneNote-dokument?

S1: Ja, Aspose.Note för .NET låter dig skapa, redigera och manipulera OneNote-dokument programmatiskt.

### F2: Stöder Aspose.Note laddningshistorik för alla typer av OneNote-filer?

S2: Aspose.Note stöder laddningshistorik för både .one och .onepkg filformat.

### F3: Finns det en gratis testversion tillgänglig för Aspose.Note för .NET?

 S3: Ja, du kan ladda ner en gratis testversion av Aspose.Note för .NET från[här](https://releases.aspose.com/).

### F4: Hur kan jag få en tillfällig licens för Aspose.Note för .NET?

 S4: Du kan begära en tillfällig licens från[den här länken](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag hitta support för Aspose.Note för .NET?

 S5: Du kan hitta support och resurser på[Aspose.Note forum](https://forum.aspose.com/c/note/28).