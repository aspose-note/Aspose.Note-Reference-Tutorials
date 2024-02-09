---
title: Markera alla senaste ändringar i Aspose.Note-text
linktitle: Markera alla senaste ändringar i Aspose.Note-text
second_title: Aspose.Note .NET API
description: Förbättra dina anteckningsdokument med Aspose.Note för .NET! Lär dig hur du markerar de senaste ändringarna i text med denna steg-för-steg-handledning.
type: docs
weight: 19
url: /sv/net/text-manipulation/highlight-recent-changes/
---
## Introduktion
Vill du lägga till dynamiska och visuellt tilltalande funktioner till dina Note-dokument med hjälp av .NET? Aspose.Note för .NET är en kraftfull lösning som låter dig manipulera och förbättra dina Note-filer sömlöst. I den här handledningen kommer vi att dyka in i en specifik aspekt: att markera alla senaste ändringar i Aspose.Note-text.
## Förutsättningar
Innan vi ger oss ut på denna resa, se till att du har följande förutsättningar på plats:
-  Aspose.Note för .NET: Se till att du har Aspose.Note-biblioteket installerat. Du kan ladda ner den från[Aspose.Note för .NET-dokumentation](https://reference.aspose.com/note/net/).
- Utvecklingsmiljö: Konfigurera en .NET-utvecklingsmiljö, inklusive en IDE som Visual Studio.
- Exempeldokument: Förbered ett anteckningsdokument (i det här fallet "Aspose.one") som innehåller texten du vill markera.
## Importera namnområden
För att komma igång, importera nödvändiga namnområden i ditt .NET-projekt:
```csharp
    using System;
    using System.Drawing;
    using System.IO;
    using System.Linq;
```
## Steg 1: Ladda dokumentet
Börja med att ladda anteckningsdokumentet i Aspose.Note:
```csharp
string dataDir = "Your Document Directory";
Document document = new Document(dataDir + "Aspose.one");
```
## Steg 2: Identifiera de senaste ändringarna
Identifiera sedan RichText-noder som ändrats under den senaste veckan:
```csharp
var richTextNodes = document.GetChildNodes<RichText>().Where(e => e.LastModifiedTime >= DateTime.Today.Subtract(TimeSpan.FromDays(7)));
```
## Steg 3: Ställ in markeringsfärger
Ställ nu in markeringsfärgen för de identifierade noderna och textkörningarna:
```csharp
foreach (var node in richTextNodes)
{
    // Ställ in markeringsfärg för stycke
    node.ParagraphStyle.Highlight = Color.DarkGreen;
    // Ställ in markeringsfärg för varje textkörning
    foreach (var run in node.TextRuns)
    {
        run.Style.Highlight = Color.DarkSeaGreen;
    }
}
```
## Steg 4: Spara det ändrade dokumentet
Spara dokumentet med markerade senaste ändringar:
```csharp
document.Save(Path.Combine(dataDir, "HighlightAllRecentChanges.pdf"));
```
## Steg 5: Visa framgångsmeddelande
Till sist, visa ett framgångsmeddelande för att informera användaren:
```csharp
Console.WriteLine("\nText's recent changes are highlighted successfully.");
```
## Slutsats
I den här handledningen undersökte vi hur man använder Aspose.Note för .NET för att markera alla senaste ändringar i text i ett Note-dokument. Den här funktionen förbättrar dokumentets synlighet och är ett värdefullt tillägg till din verktygslåda för att arbeta med anteckningsfiler.
## Vanliga frågor
### Kan jag använda olika högdagerfärger för olika tidsperioder?
Ja, du kan anpassa koden för att ställa in olika höjdpunkter baserat på dina specifika krav.
### Är Aspose.Note kompatibel med de senaste .NET-ramverken?
Aspose.Note uppdaterar regelbundet sina bibliotek för att säkerställa kompatibilitet med de senaste .NET-ramverken.
### Hur kan jag hantera fel när jag implementerar den här funktionen?
Du kan införliva försöksfångstblock för att hantera undantag och ge en smidig användarupplevelse.
### Stöder Aspose.Note andra textformateringsfunktioner?
Absolut! Aspose.Note tillhandahåller ett brett utbud av funktioner för textformatering, inklusive teckensnitt, storlekar och mer.
### Kan jag integrera denna lösning i en webbapplikation?
Ja, du kan integrera Aspose.Note för .NET i webbapplikationer för att förbättra dokumentbehandlingskapaciteten.