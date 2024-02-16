---
title: Använd numrering på text i Aspose.Note
linktitle: Använd numrering på text i Aspose.Note
second_title: Aspose.Note .NET API
description: Lär dig hur du använder textnumrering i Aspose.Note för .NET med denna omfattande handledning. Förbättra din dokumentformatering utan ansträngning.
type: docs
weight: 12
url: /sv/net/text-manipulation/apply-numbering-on-text/
---
## Introduktion
Aspose.Note för .NET tillhandahåller kraftfulla verktyg för dokumenthantering i C#-applikationer. I den här handledningen kommer vi att utforska processen att tillämpa numrering på text med Aspose.Note. Följ dessa steg-för-steg-instruktioner för att förbättra din dokumentformatering utan ansträngning.
## Förutsättningar
Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:
- Grundläggande förståelse för programmeringsspråket C#.
-  Aspose.Note för .NET installerat. Du kan ladda ner den[här](https://releases.aspose.com/note/net/).
- En integrerad utvecklingsmiljö (IDE) som Visual Studio.
## Importera namnområden
För att komma igång, se till att importera de nödvändiga namnrymden i ditt C#-projekt:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Drawing;
using System.Collections.Generic;
```
## Steg 1: Konfigurera ditt dokument
Börja med att skapa ett nytt dokument och initiera de nödvändiga objekten:
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";
//Skapa ett objekt av klassen Document
Document doc = new Document();
// Initiera Sidklassobjekt
Aspose.Note.Page page = new Aspose.Note.Page(doc);
// Initiera Outline-klassobjekt
Outline outline = new Outline(doc);
```
## Steg 2: Definiera standardstil
Ställ in standardstilen för din text med klassen ParagraphStyle:
```csharp
ParagraphStyle defaultStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
```
## Steg 3: Använd numrering
Initiera OutlineElement-klassobjekt och tillämpa numrering på varje element:
```csharp
OutlineElement outlineElem1 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text1 = new RichText(doc) { Text = "First", ParagraphStyle = defaultStyle };
outlineElem1.AppendChildLast(text1);
OutlineElement outlineElem2 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text2 = new RichText(doc) { Text = "Second", ParagraphStyle = defaultStyle };
outlineElem2.AppendChildLast(text2);
OutlineElement outlineElem3 = new OutlineElement(doc) { NumberList = new NumberList("{0})", NumberFormat.DecimalNumbers, "Arial", 10) };
RichText text3 = new RichText(doc) { Text = "Third", ParagraphStyle = defaultStyle };
outlineElem3.AppendChildLast(text3);
```
## Steg 4: Lägg till dispositionselement
Lägg till dispositionselementen till dispositionen:
```csharp
outline.AppendChildLast(outlineElem1);
outline.AppendChildLast(outlineElem2);
outline.AppendChildLast(outlineElem3);
```
## Steg 5: Spara dokumentet
Spara OneNote-dokumentet med den tillämpade numreringen:
```csharp
dataDir = dataDir + "ApplyNumberingOnText_out.one"; 
doc.Save(dataDir);
Console.WriteLine("\nNumbering applied successfully on a text.\nFile saved at " + dataDir); 
```
## Slutsats
Grattis! Du har framgångsrikt lärt dig hur man använder numrering på text i Aspose.Note för .NET. Experimentera med olika formateringsalternativ för att skapa visuellt tilltalande dokument utan ansträngning.
## FAQ's
### 1. Kan jag anpassa numreringsformatet?
Ja, klassen NumberList låter dig anpassa numreringsformatet enligt dina preferenser.
### 2. Finns det andra formateringsalternativ?
Aspose.Note erbjuder ett brett utbud av formateringsalternativ, inklusive typsnittsstil, färg och mer.
### 3. Är Aspose.Note kompatibel med Visual Studio?
Absolut! Aspose.Note integreras sömlöst med Visual Studio för en smidig utvecklingsupplevelse.
### 4. Kan jag prova Aspose.Note innan jag köper?
 Säkert! Du kan utforska en gratis provperiod[här](https://releases.aspose.com/).
### 5. Var kan jag få support för Aspose.Note?
 För all hjälp eller frågor, besök[Aspose.Note forum](https://forum.aspose.com/c/note/28).