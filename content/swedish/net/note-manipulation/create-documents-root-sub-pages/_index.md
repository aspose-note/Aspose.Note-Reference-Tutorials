---
title: Skapa dokument med rot- och undersidor med Aspose.Note
linktitle: Skapa dokument med rot- och undersidor med Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du använder Aspose.Note för .NET för att skapa dynamiska OneNote-dokument med hierarkiska strukturer.
type: docs
weight: 11
url: /sv/net/note-manipulation/create-documents-root-sub-pages/
---
## Introduktion

Välkommen till vår handledning om att skapa dokument med rot- och undersidor med Aspose.Note för .NET! Aspose.Note är ett kraftfullt bibliotek som gör det möjligt för utvecklare att arbeta med Microsoft OneNote-filer programmatiskt, vilket gör det möjligt att skapa, manipulera och konvertera OneNote-dokument.

den här handledningen går vi igenom processen att skapa ett OneNote-dokument med rot- och undersidor steg för steg. Vi kommer att tillhandahålla detaljerade förklaringar och kodavsnitt med Aspose.Note för .NET, vilket gör det enkelt för dig att följa med och implementera i dina egna projekt.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar:

1. Visual Studio: Du behöver Visual Studio installerat på ditt system för att skriva och kompilera .NET-kod.
2.  Aspose.Note for .NET: Ladda ner och installera Aspose.Note for .NET från[nedladdningssida](https://releases.aspose.com/note/net/).
3. Grundläggande C#-kunskaper: Förtrogenhet med C#-programmeringsspråket krävs för att förstå och implementera kodexemplen.

Nu när du har allt inställt, låt oss dyka in i handledningen!

## Importera namnområden

Låt oss först importera de nödvändiga namnrymden till vårt projekt:

```csharp
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using System.Drawing;
```

## Steg 1: Initiera dokumentobjekt

```csharp
// Skapa ett objekt av klassen Document
Document doc = new Document();
```

## Steg 2: Skapa rotsida och undersidor

```csharp
// Initiera sidklassobjekt och ställ in deras nivåer
Page page1 = new Page(doc) { Level = 1 };
Page page2 = new Page(doc) { Level = 2 };
Page page3 = new Page(doc) { Level = 1 };
```

### För sida 1:

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
ParagraphStyle textStyle1 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text1 = new RichText(doc) { Text = "First page.", ParagraphStyle = textStyle1 };
outlineElem1.AppendChildLast(text1);
outline1.AppendChildLast(outlineElem1);
page1.AppendChildLast(outline1);
```

### För sida 2:

```csharp
Outline outline2 = new Outline(doc);
OutlineElement outlineElem2 = new OutlineElement(doc);
ParagraphStyle textStyle2 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text2 = new RichText(doc) { Text = "Second page.", ParagraphStyle = textStyle2 };
outlineElem2.AppendChildLast(text2);
outline2.AppendChildLast(outlineElem2);
page2.AppendChildLast(outline2);
```

### För sida 3:

```csharp
Outline outline3 = new Outline(doc);
OutlineElement outlineElem3 = new OutlineElement(doc);
ParagraphStyle textStyle3 = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
RichText text3 = new RichText(doc) { Text = "Third page.", ParagraphStyle = textStyle3 };
outlineElem3.AppendChildLast(text3);
outline3.AppendChildLast(outlineElem3);
page3.AppendChildLast(outline3);
```

## Steg 4: Lägg till sidor i dokument

```csharp
// Lägg till sidor i OneNote-dokumentet
doc.AppendChildLast(page1);
doc.AppendChildLast(page2);
doc.AppendChildLast(page3);
```

## Steg 5: Spara dokument

```csharp
// Spara OneNote-dokument
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithRootAndSubPages_out.one";
doc.Save(dataDir);
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du skapar dokument med rot- och undersidor med Aspose.Note för .NET. Nu kan du använda denna kunskap för att dynamiskt generera komplexa OneNote-dokument i dina applikationer.

## FAQ's

### F1: Kan Aspose.Note hantera stora OneNote-dokument?

S1: Ja, Aspose.Note är utformad för att effektivt hantera stora OneNote-dokument utan att kompromissa med prestanda.

### F2: Är Aspose.Note kompatibel med .NET Core?

S2: Ja, Aspose.Note stöder .NET Core tillsammans med det traditionella .NET Framework.

### F3: Kan jag konvertera OneNote-dokument till andra format med Aspose.Note?

S3: Absolut, Aspose.Note tillhandahåller konverteringsmöjligheter till olika format inklusive PDF, DOCX, HTML och mer.

### F4: Erbjuder Aspose.Note molnintegration?

S4: Aspose.Note fokuserar i första hand på lokal utveckling, men du kan använda det i molnmiljöer med rätt inställning.

### F5: Finns teknisk support tillgänglig för Aspose.Note?

S5: Ja, Aspose tillhandahåller dedikerad teknisk support genom deras forum där du kan ställa frågor och få hjälp.