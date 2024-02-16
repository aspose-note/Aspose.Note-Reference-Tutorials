---
title: Använd punkter på text i Aspose.Note
linktitle: Använd punkter på text i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du använder punkter på text i Aspose.Note för .NET för att förbättra dina OneNote-dokument. Följ denna steg-för-steg-guide för effektiv formatering.
type: docs
weight: 10
url: /sv/net/text-manipulation/apply-bullets-on-text/
---
## Introduktion
Välkommen till den här steg-för-steg-guiden för att applicera punkter på text med Aspose.Note för .NET. Aspose.Note är ett kraftfullt bibliotek som låter utvecklare arbeta sömlöst med Microsoft OneNote-filer i sina .NET-applikationer. I den här handledningen kommer vi att leda dig genom processen att applicera punktpunkter på text, vilket förbättrar det visuella tilltalande av dina OneNote-dokument.
## Förutsättningar
Innan vi dyker in i handledningen, se till att du har följande förutsättningar:
- Grundläggande kunskaper i C# och .NET programmering.
-  Aspose.Note för .NET-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/note/net/).
## Importera namnområden
Se till att inkludera de nödvändiga namnrymden i din C#-kod:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Steg 1: Konfigurera ditt dokument
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";
//Skapa ett objekt av klassen Document
Aspose.Note.Document doc = new Aspose.Note.Document();
```
## Steg 2: Initiera sida och disposition
```csharp
// Initiera Sidklassobjekt
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Initiera Outline-klassobjekt
Outline outline = new Outline(doc);
```
## Steg 3: Ställ in standardtextstil
```csharp
// Initiera TextStyle-klassobjekt och ställ in formateringsegenskaper
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Steg 4: Skapa konturelement med punkter
```csharp
// Initiera OutlineElement-klassobjekt och använd kulor
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("*", "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
// Upprepa för andra konturelement
```
## Steg 5: Lägg till dispositionselement till dispositionen
```csharp
// Lägg till konturelement
outline.AppendChildLast(outlineElem1);
// Upprepa för andra konturelement
```
## Steg 6: Lägg till Outline på sidan
```csharp
// Lägg till Outline-nod
page.AppendChildLast(outline);
```
## Steg 7: Lägg till sida i dokumentet
```csharp
//Lägg till sidnod
doc.AppendChildLast(page);
```
## Steg 8: Spara OneNote-dokumentet
```csharp
// Spara OneNote-dokument
dataDir = dataDir + "ApplyBulletsOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nBullets applied successfully on a text.\nFile saved at " + dataDir); 
```
## Slutsats
Grattis! Du har framgångsrikt lärt dig hur du applicerar punktpunkter på text med Aspose.Note för .NET. Den här funktionen kan avsevärt förbättra formateringen av dina OneNote-dokument, vilket gör dem mer visuellt tilltalande.
## FAQ's
### Kan jag använda olika punktstilar på varje objekt i listan?
 Ja, du kan anpassa kulstilarna genom att ändra`NumberList` fastigheter för varje`OutlineElement`.
### Är Aspose.Note kompatibel med den senaste versionen av Microsoft OneNote?
Aspose.Note stöder olika versioner av Microsoft OneNote, vilket säkerställer kompatibilitet med både äldre och nyare versioner.
### Kan jag använda Aspose.Note för kommersiella ändamål?
 Ja, du kan använda Aspose.Note för .NET i kommersiella projekt. För att få en licens, besök[här](https://purchase.aspose.com/buy).
### Finns det en testversion tillgänglig för Aspose.Note för .NET?
 Ja, du kan ladda ner en gratis testversion[här](https://releases.aspose.com/).
### Var kan jag hitta ytterligare support och resurser?
 Du kan besöka Aspose.Note-gemenskapsforumet[här](https://forum.aspose.com/c/note/28) för stöd och diskussioner.