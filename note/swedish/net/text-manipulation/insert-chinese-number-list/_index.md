---
title: Infoga kinesisk nummerlista i Aspose.Note-texten
linktitle: Infoga kinesisk nummerlista i Aspose.Note-texten
second_title: Aspose.Note .NET API
description: Lär dig hur du infogar kinesiska nummerlistor i Aspose.Note för .NET-dokument utan ansträngning. Öka dina färdigheter i dokumentformatering med denna steg-för-steg-guide.
weight: 20
url: /sv/net/text-manipulation/insert-chinese-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Infoga kinesisk nummerlista i Aspose.Note-texten

## Introduktion
Vill du förbättra dina kunskaper i Aspose.Note för .NET genom att införliva kinesiska nummerlistor i dina dokument? I så fall är du på rätt plats! I den här handledningen går vi igenom processen för att infoga kinesiska nummerlistor med Aspose.Note för .NET. Detta kraftfulla bibliotek låter dig manipulera OneNote-dokument sömlöst.
## Förutsättningar
Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:
- Grundläggande kunskaper i C#-programmering.
-  Aspose.Note för .NET installerat. Du kan ladda ner den[här](https://releases.aspose.com/note/net/).
## Importera namnområden
För att komma igång, importera de nödvändiga namnområdena till ditt projekt:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Steg 1: Initiera OneNote-dokument
```csharp
string dataDir = "Your Document Directory";
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Steg 2: Initiera OneNote-sidan
```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
Outline outline = new Outline(doc);
```
## Steg 3: Använd textstilsinställningar
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Steg 4: Skapa dispositionselement
Låt oss nu skapa tre konturelement med kinesiska nummerlistor:
### Steg 4.1: Första elementet
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
```
### Steg 4.2: Andra elementet
```csharp
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
```
### Steg 4.3: Tredje elementet
```csharp
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.ChineseCounting, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Steg 5: Lägg till element till Outline
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Steg 6: Lägg till disposition till sidan
```csharp
page.AppendChildLast(outline);
```
## Steg 7: Lägg till sida till dokument
```csharp
doc.AppendChildLast(page);
```
## Steg 8: Spara OneNote-dokument
```csharp
dataDir = dataDir + "InsertChineseNumberList_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nChinese number list inserted successfully.\nFile saved at " + dataDir);
```
Grattis! Du har framgångsrikt infogat kinesiska nummerlistor i ditt Aspose.Note-dokument med hjälp av .NET-biblioteket.
## Slutsats
I den här handledningen täckte vi steg-för-steg-processen för att införliva kinesiska nummerlistor i dina Aspose.Note för .NET-dokument. Förbättra dina färdigheter i dokumentformatering och gör ditt innehåll mer engagerande med dessa tekniker.
## Vanliga frågor
### F: Kan jag anpassa formateringen av kinesiska nummerlistor?
 S: Ja, du kan anpassa formateringen genom att justera parametrarna i`NumberList` konstruktör.
### F: Är Aspose.Note kompatibel med den senaste versionen av .NET?
S: Ja, Aspose.Note uppdateras regelbundet för att stödja de senaste versionerna av .NET.
### F: Var kan jag hitta ytterligare exempel och dokumentation?
S: Utforska det omfattande[Aspose.Note dokumentation](https://reference.aspose.com/note/net/).
### F: Hur kan jag få en tillfällig licens för Aspose.Note?
 S: Skaffa en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).
### F: Var kan jag söka hjälp eller diskutera Aspose.Note-relaterade frågor?
 A: Besök[Aspose.Note supportforum](https://forum.aspose.com/c/note/28) för samhällsstöd.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
