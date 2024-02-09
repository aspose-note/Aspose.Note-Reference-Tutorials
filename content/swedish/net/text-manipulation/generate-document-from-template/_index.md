---
title: Generera dokument från mall i Aspose.Note
linktitle: Generera dokument från mall i Aspose.Note
second_title: Aspose.Note .NET API
description: Generera dynamiska dokument utan ansträngning med Aspose.Note för .NET. Följ vår steg-för-steg-guide för personligt och datadrivet dokumentskapande.
type: docs
weight: 18
url: /sv/net/text-manipulation/generate-document-from-template/
---
## Introduktion
I det ständigt föränderliga landskapet för dokumentskapande framstår Aspose.Note för .NET som ett kraftfullt verktyg för att generera dynamiska dokument utan ansträngning. Oavsett om du har att göra med rapporter, fakturor eller personliga dokument, kommer den här handledningen att guida dig genom processen att skapa ett dokument från en mall med Aspose.Note för .NET.
## Förutsättningar
Innan du dyker in i steg-för-steg-guiden, se till att du har följande förutsättningar på plats:
1.  Aspose.Note för .NET Library: Ladda ner och installera biblioteket från[Aspose.Note för .NET-dokumentation](https://reference.aspose.com/note/net/).
2. Dokumentmall: Förbered ett malldokument i OneNote-formatet (med tillägget .one). Detta kommer att fungera som grunden för ditt dynamiskt genererade dokument.
## Importera namnområden
Se till att inkludera nödvändiga namnutrymmen i ditt projekt:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Låt oss nu dela upp varje steg i guiden.
## Steg 1: Definiera din dokumentkatalog
```csharp
string dataDir = "Your Document Directory";
```
Ersätt "Din dokumentkatalog" med sökvägen där du vill spara ditt genererade dokument.
## Steg 2: Skapa en ordbok med ersättningsvärden
```csharp
var templateData = new Dictionary<string, string>
{
    { "Company", "Atlas Shrugged Ltd" },
    { "CandidateName", "John Galt" },
    { "JobTitle", "Chief Entrepreneur Officer" },
    { "Department", "Sales" },
    { "Salary", "123456 USD" },
    { "Vacation", "30" },
    { "StartDate", "29 Feb 2024" },
    { "YourName", "Ayn Rand" }
};
```
Definiera en ordbok där nycklarna är platshållare i din mall och värden är de data du vill ersätta dem med.

## Steg 3: Ladda malldokumentet
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Ladda ditt OneNote-malldokument i Aspose.Note.

## Steg 4: Ersätt mallord med dynamiska data
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Iterera genom varje stycke i mallen och ersätt platshållare med dynamisk data.

## Steg 5: Spara det genererade dokumentet
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Spara det dynamiskt genererade dokumentet i din angivna katalog.

## Slutsats
Grattis! Du har framgångsrikt skapat ett dynamiskt dokument med Aspose.Note för .NET. Denna process öppnar en värld av möjligheter för att skapa personliga och datadrivna dokument sömlöst.

## Vanliga frågor
### Kan jag använda Aspose.Note för .NET med andra dokumentformat?
Ja, Aspose.Note för .NET hanterar i första hand OneNote-dokument, men Aspose tillhandahåller olika bibliotek för olika format.
### Finns det en gratis testversion tillgänglig för Aspose.Note för .NET?
 Ja, du kan utforska funktionerna i Aspose.Note för .NET med en gratis provperiod. Besök[här](https://releases.aspose.com/) för mer information.
### Hur kan jag få support för Aspose.Note för .NET?
 Besök[Aspose.Note för .NET-forum](https://forum.aspose.com/c/note/28) för att få hjälp från samhället och experter.
### Finns tillfälliga licenser tillgängliga för Aspose.Note för .NET?
 Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för test- och utvärderingsändamål.
### Var kan jag hitta omfattande dokumentation för Aspose.Note för .NET?
 Referera till[dokumentation](https://reference.aspose.com/note/net/) för djupgående information om hur du använder Aspose.Note för .NET.