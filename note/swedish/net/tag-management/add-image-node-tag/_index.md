---
title: Lägg till bildnod med tagg i Aspose.Note
linktitle: Lägg till bildnod med tagg i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du förbättrar dina OneNote-dokument genom att lägga till bilder med anpassade taggar med Aspose.Note för .NET.
type: docs
weight: 10
url: /sv/net/tag-management/add-image-node-tag/
---
## Introduktion

I den här handledningen kommer vi att utforska hur man lägger till en bildnod med en tagg med Aspose.Note för .NET. Den här funktionen låter dig förbättra dina OneNote-dokument genom att lägga till bilder med anpassade taggar.

## Förutsättningar

Innan du börjar, se till att du har följande:

1. Visual Studio: Installera Visual Studio IDE på ditt system.
2.  Aspose.Note for .NET: Ladda ner och installera Aspose.Note for .NET-biblioteket från[nedladdningslänk](https://releases.aspose.com/note/net/).
3. Grundläggande kunskaper: Bekanta dig med programmeringsspråket C# och .NET framework.

## Importera namnområden

Se först till att inkludera de nödvändiga namnrymden i din C#-kod:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
```

## Steg 1: Initiera dokument- och sidobjekt

 Börja med att skapa en instans av`Document` klass och a`Page` objekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Steg 2: Initiera Outline- och OutlineElement-objekt

 Initiera sedan`Outline` och`OutlineElement` föremål:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
```

## Steg 3: Ladda och infoga bild

Ladda önskad bild och infoga den i dokumentnoden:

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, "path_to_your_image.jpg");
outlineElem.AppendChildLast(image);
```

## Steg 4: Lägg till tagg till bilden

Lägg till en anpassad tagg till bilden:

```csharp
image.Tags.Add(NoteTag.CreateYellowStar());
```

## Steg 5: Lägg till dispositionselement och sidnoder

Lägg till konturelementet och konturnoderna på sidan:

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
```

## Steg 6: Spara dokumentet

Spara det ändrade OneNote-dokumentet:

```csharp
doc.AppendChildLast(page);
string outputFilePath = "output_path/AddImageNodeWithTag_out.one";
doc.Save(outputFilePath);
```

## Slutsats

Genom att följa dessa steg kan du sömlöst lägga till en bildnod med en anpassad tagg med Aspose.Note för .NET, vilket berikar dina OneNote-dokument med personliga bilder.

## FAQ's

### F1: Kan jag lägga till flera bilder med olika taggar i ett enda dokument med Aspose.Note?

S1: Ja, du kan lägga till flera bilder med olika taggar genom att följa liknande steg för varje bild.

### F2: Är Aspose.Note kompatibel med alla versioner av OneNote?

S2: Aspose.Note stöder olika versioner av OneNote, vilket säkerställer kompatibilitet mellan olika miljöer.

### F3: Kan jag anpassa utseendet på taggen som lagts till i bilden?

S3: Ja, Aspose.Note ger flexibilitet när det gäller att anpassa taggens utseende för att passa dina preferenser.

### F4: Erbjuder Aspose.Note stöd för att lägga till bilder från webbadresser?

S4: Aspose.Note stöder i första hand att lägga till bilder från lokala kataloger, men du kan införliva externa bilder genom att ladda ner dem lokalt först.

### F5: Finns det några begränsningar för storleken eller formatet på bilder som kan läggas till?

S5: Aspose.Note stöder ett brett utbud av bildformat och ställer inga strikta begränsningar på bildstorleken, vilket gör att du kan införliva olika bilder i dina dokument.