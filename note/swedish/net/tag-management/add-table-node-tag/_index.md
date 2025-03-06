---
title: Lägg till tabellnod med tagg i Aspose.Note
linktitle: Lägg till tabellnod med tagg i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du lägger till tabeller med taggar i Aspose.Note för .NET. Förbättra dina dokumenthanteringsfärdigheter programmatiskt.
weight: 11
url: /sv/net/tag-management/add-table-node-tag/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägg till tabellnod med tagg i Aspose.Note

## Introduktion

I den här handledningen guidar vi dig genom processen att lägga till en tabellnod med en tagg med Aspose.Note för .NET. Följ stegen nedan för att uppnå detta.

## Importera namnområden

Innan du börjar, se till att importera de nödvändiga namnrymden för att arbeta med Aspose.Note:

```csharp
using System.Drawing;
using System.IO;
using Aspose.Note;
using System;
using System.Collections.Generic;
using Aspose.Note.Examples.CSharp.Tables;
```

## Förutsättningar

Se till att du har ställt in följande förutsättningar innan du fortsätter:

1.  Installation: Ladda ner och installera Aspose.Note för .NET-biblioteket från[här](https://releases.aspose.com/note/net/).
2.  Licens: Skaffa en licens eller använd en[tillfällig licens](https://purchase.aspose.com/temporary-license/) att använda biblioteket.
3. Utvecklingsmiljö: Ha en kompatibel utvecklingsmiljö inrättad, som Visual Studio.

## Steg 1: Initiera dokument- och sidobjekt

 Börja med att skapa en instans av`Document` klass och initialisering av a`Page` objekt:

```csharp
Document doc = new Document();
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

## Steg 2: Skapa tabell-, rad- och cellobjekt

 Initiera`Table`, `TableRow` , och`TableCell` föremål:

```csharp
TableRow row = new TableRow(doc);
TableCell cell = new TableCell(doc);
```

## Steg 3: Infoga innehåll i cellen

 Lägg till innehåll i cellen genom att använda`AppendChildLast` metod:

```csharp
cell.AppendChildLast(InsertTable.GetOutlineElementWithText(doc, "Single cell."));
```

## Steg 4: Initiera tabellnoden

 Initiera`Table` objekt med specificerade egenskaper:

```csharp
Table table = new Table(doc)
{
    IsBordersVisible = true,
    Columns = { new TableColumn { Width = 70 } }
};
```

## Steg 5: Lägg till rad i tabellen

Lägg till radnoden i tabellen:

```csharp
table.AppendChildLast(row);
```

## Steg 6: Lägg till tagg till tabellnoden

Inkludera en tagg för tabellnoden:

```csharp
table.Tags.Add(NoteTag.CreateQuestionMark());
```

## Steg 7: Lägg till tabellnod till konturelement

 Skapa en`Outline` och`OutlineElement` för att lägga till tabellnoden:

```csharp
Outline outline = new Outline(doc);
OutlineElement outlineElem = new OutlineElement(doc);
outlineElem.AppendChildLast(table);
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Steg 8: Spara dokument

Spara OneNote-dokumentet:

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "AddTableNodeWithTag_out.one";
doc.Save(dataDir);
Console.WriteLine("\nTable node with tag added successfully.\nFile saved at " + dataDir);
```

Efter att ha följt dessa steg bör du ha lagt till en tabellnod med en tagg med Aspose.Note för .NET.

## Slutsats

I den här handledningen har vi täckt processen att lägga till en tabellnod med en tagg i Aspose.Note för .NET. Genom att följa dessa steg kan du effektivt manipulera OneNote-dokument programmässigt, vilket förbättrar dina dokumenthanteringsmöjligheter.

## FAQ's

### F1: Är Aspose.Note kompatibel med alla versioner av .NET?

S1: Aspose.Note för .NET stöder .NET Framework version 2.0 och högre, inklusive .NET Core och .NET Standard.

### F2: Kan jag prova Aspose.Note innan jag köper en licens?

 S2: Ja, du kan få en gratis provversion av Aspose.Note från[här](https://releases.aspose.com/).

### F3: Hur skaffar jag en tillfällig licens för Aspose.Note?

 A3: Du kan få en tillfällig licens från[den här länken](https://purchase.aspose.com/temporary-license/), som gäller i 30 dagar.

### F4: Stöder Aspose.Note dokumentkryptering?

S4: Ja, Aspose.Note tillhandahåller stöd för kryptering av OneNote-dokument för att säkerställa datasäkerhet.

### F5: Finns teknisk support tillgänglig för Aspose.Note-användare?

 S5: Ja, teknisk support tillhandahålls via Aspose-forumen[här](https://forum.aspose.com/c/note/28), där du kan söka hjälp från experter.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
