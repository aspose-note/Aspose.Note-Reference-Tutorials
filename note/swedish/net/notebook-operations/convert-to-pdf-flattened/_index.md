---
title: Konvertera anteckningsböcker till PDF (tillplattade) i Aspose Note .NET
linktitle: Konvertera anteckningsböcker till PDF (tillplattade) i Aspose Note .NET
second_title: Aspose.Note .NET API
description: Lär dig hur du enkelt konverterar OneNote-anteckningsböcker till tillplattade PDF-filer med Aspose.Note för .NET. Bevara ditt innehåll sömlöst.
weight: 15
url: /sv/net/notebook-operations/convert-to-pdf-flattened/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera anteckningsböcker till PDF (tillplattade) i Aspose Note .NET

## Introduktion

Vill du konvertera dina OneNote-anteckningsböcker till tillplattade PDF-filer med Aspose Note .NET? Du är på rätt plats! I den här handledningen går vi igenom processen steg för steg.

## Förutsättningar

Innan vi börjar, se till att du har följande:

1.  Aspose.Note for .NET: Se till att du har laddat ner och installerat Aspose.Note for .NET. Om inte, kan du få det från[här](https://releases.aspose.com/note/net/).
2. Visual Studio: Du behöver Visual Studio installerat på ditt system för kodning och kompilering.
3. OneNote Notebook: Ha en OneNote Notebook redo som du vill konvertera till en PDF.

## Importera namnområden

Låt oss börja med att importera de nödvändiga namnrymden i din C#-kod:

```csharp
using System.IO;
using Aspose.Note;
using Aspose.Note.Saving;
using System;
using System.Collections.Generic;
```

## Steg 1: Ladda OneNote Notebook

```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";

// Ladda en OneNote-anteckningsbok
var notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

 I det här steget laddar vi OneNote Notebook med hjälp av`Notebook` klass tillhandahållen av Aspose.Note.

## Steg 2: Konvertera till PDF med Flattening

```csharp
// Spara anteckningsboken som PDF med tillplattning
dataDir = dataDir + "ConvertToPDFAsFlattened_out.pdf";
notebook.Save(
    dataDir,
    new NotebookPdfSaveOptions
    {
        Flatten = true
    }); 
```

 Här sparar vi den laddade anteckningsboken som en PDF med`Flatten` egenskapen inställd på`true`. Den här egenskapen plattar ut allt innehåll, inklusive kommentarer och bilder, till PDF-filen.

## Steg 3: Skriv ut meddelande om framgång

```csharp
Console.WriteLine("\nNoteBook document converted to PDF as flattened successfully.\nFile saved at " + dataDir);
```

Slutligen skriver vi ut ett framgångsmeddelande tillsammans med sökvägen där PDF:en sparas.

## Slutsats

Grattis! Du har framgångsrikt konverterat din OneNote Notebook till en tillplattad PDF med Aspose.Note för .NET. Denna process säkerställer att allt ditt innehåll bevaras korrekt i PDF-format, vilket gör det lättare att dela och distribuera.

## FAQ's

### F1: Kan jag bevara interaktiva element i PDF-filen?

S1: Aspose.Note plattar ut innehållet, inklusive interaktiva element som kryssrutor eller formulärfält, till PDF-filen, vilket gör dem statiska.

### F2: Har Aspose.Note stöd för att konvertera bärbara datorer till andra format?

S2: Ja, Aspose.Note stöder konvertering av anteckningsböcker till olika format som PDF, HTML, bild och mer.

### F3: Kan jag anpassa konverteringsalternativen?

A3: Absolut! Aspose.Note tillhandahåller omfattande alternativ för anpassning under konverteringsprocessen, så att du kan skräddarsy resultatet efter dina krav.

### F4: Finns det en testversion tillgänglig?

 A4: Ja, du kan få en gratis provversion av Aspose.Note från[här](https://releases.aspose.com/).

### F5: Var kan jag få support om jag stöter på några problem?

 S5: Du kan söka stöd från Aspose-gemenskapen på[Aspose.Note-forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
