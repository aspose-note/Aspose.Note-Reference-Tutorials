---
title: Hämta punktlista eller nummerlista i Aspose.Note-text
linktitle: Hämta punktlista eller nummerlista i Aspose.Note-text
second_title: Aspose.Note .NET API
description: Lås upp potentialen hos Aspose.Note för .NET med vår steg-för-steg-guide för att hämta punkt- eller nummerlistor. Öka dina färdigheter i OneNote-dokumenthantering!
type: docs
weight: 23
url: /sv/net/text-manipulation/retrieve-bullet-number-list/
---
## Introduktion
Välkommen till Aspose.Note-världen för .NET, ett robust och mångsidigt bibliotek som ger utvecklare möjlighet att hantera OneNote-dokumentmanipulation utan ansträngning. I den här handledningen kommer vi att fördjupa oss i processen för att hämta punktlistor eller nummerlistor med Aspose.Note för .NET. Oavsett om du är en erfaren utvecklare eller en kodningsentusiast, kommer den här guiden att utrusta dig med kunskapen för att navigera genom krångligheterna med att arbeta med listor i Aspose.Note.
## Förutsättningar
Innan vi ger oss ut på denna kodningsresa, se till att du har följande förutsättningar på plats:
-  Aspose.Note för .NET: Se till att du har Aspose.Note-biblioteket installerat. Om inte kan du ladda ner den från[Aspose.Note för .NET-dokumentation](https://reference.aspose.com/note/net/).
- Utvecklingsmiljö: Ha en fungerande utvecklingsmiljö, helst Microsoft Visual Studio, inställd på din maskin.
- Grundläggande kunskaper om C#: Bekanta dig med C# eftersom denna handledning är skriven på detta språk.
## Importera namnområden
För att kunna interagera med Aspose.Note för .NET måste du importera de nödvändiga namnrymden till ditt projekt. Inkludera följande namnrymder i början av koden:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Låt oss nu bryta ner processen för att hämta punkt- eller nummerlistor steg för steg:
## Steg 1: Ställ in din dokumentkatalog
```csharp
// Sökvägen till dokumentkatalogen.
string dataDir = "Your Document Directory";
```
 Byta ut`"Your Document Directory"` med den faktiska sökvägen där ditt Aspose.Note-dokument finns.
## Steg 2: Ladda dokumentet
```csharp
// Ladda dokumentet i Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Se till att du byter ut`"ApplyNumberingOnText.one"` med namnet på ditt specifika OneNote-dokument.
## Steg 3: Hämta samling av noder
```csharp
// Hämta en samling noder av konturelementet.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Detta steg hämtar en samling konturnoder från det laddade dokumentet.
## Steg 4: Iterera genom varje nod
```csharp
// Iterera genom varje nod.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Fortsätt till nästa steg...
    }
}
```
Denna loop säkerställer att vi bara har att göra med noder som innehåller en nummerlista.
## Steg 5: Hämta teckensnittsinformation
```csharp
// Hämta teckensnittsnamn
Console.WriteLine("Font Name: " + list.Font);
// Hämta teckensnittslängd
Console.WriteLine("Font Length: " + list.Font.Length);
// Hämta teckenstorlek
Console.WriteLine("Font Size: " + list.FontSize);
// Hämta teckensnittsfärg
Console.WriteLine("Font Color: " + list.FontColor);
// Hämta format
Console.WriteLine("Font format: " + list.Format);
// Markera fetstil
Console.WriteLine("Is bold: " + list.IsBold);
// Markera kursiv
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Dessa kodrader extraherar olika teckensnittsrelaterad information från nummerlistan.
## Slutsats
 Grattis! Du har framgångsrikt lärt dig hur du hämtar punktlistor eller nummerlistor med Aspose.Note för .NET. När du fortsätter din utforskning, se[dokumentation](https://reference.aspose.com/note/net/) för mer djupgående insikter och funktioner.
## FAQ's
### Kan jag använda Aspose.Note för .NET med andra programmeringsspråk?
Aspose.Note stöder i första hand .NET, men det finns andra versioner av biblioteket som är skräddarsydda för olika plattformar och språk.
### Är Aspose.Note kompatibel med de senaste OneNote-formaten?
Ja, Aspose.Note stöder ett brett utbud av OneNote-format, vilket säkerställer kompatibilitet med de senaste versionerna.
### Hur kan jag få en tillfällig licens för Aspose.Note?
 Besök[den här länken](https://purchase.aspose.com/temporary-license/) för att få en tillfällig licens för utvärderingsändamål.
### Vilka supportalternativ finns tillgängliga för Aspose.Note-användare?
 Du kan utforska och söka hjälp i[Aspose.Note forum](https://forum.aspose.com/c/note/28) för alla frågor eller problem du kan stöta på.
### Finns det en gratis testversion av Aspose.Note för .NET?
 Ja, du kan komma åt den kostnadsfria testversionen av Aspose.Note för .NET[här](https://releases.aspose.com/).