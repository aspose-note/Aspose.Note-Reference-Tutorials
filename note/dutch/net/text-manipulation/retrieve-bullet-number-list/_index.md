---
title: Haal de lijst met opsommingstekens of cijfers op in Aspose.Note-tekst
linktitle: Haal de lijst met opsommingstekens of cijfers op in Aspose.Note-tekst
second_title: Aspose.Note .NET API
description: Ontgrendel het potentieel van Aspose.Note voor .NET met onze stapsgewijze handleiding voor het ophalen van lijsten met opsommingstekens of getallen. Verbeter uw vaardigheden voor het manipuleren van OneNote-documenten!
weight: 23
url: /nl/net/text-manipulation/retrieve-bullet-number-list/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Haal de lijst met opsommingstekens of cijfers op in Aspose.Note-tekst

## Invoering
Welkom in de wereld van Aspose.Note voor .NET, een robuuste en veelzijdige bibliotheek waarmee ontwikkelaars moeiteloos OneNote-documentmanipulatie kunnen verwerken. In deze zelfstudie gaan we dieper in op het proces van het ophalen van lijsten met opsommingstekens of getallen met behulp van Aspose.Note voor .NET. Of u nu een doorgewinterde ontwikkelaar of een codeerliefhebber bent, deze gids zal u voorzien van de kennis om door de fijne kneepjes van het werken met lijsten in Aspose.Note te navigeren.
## Vereisten
Voordat we aan dit codeertraject beginnen, moet je ervoor zorgen dat je aan de volgende vereisten voldoet:
-  Aspose.Note voor .NET: Zorg ervoor dat de Aspose.Note-bibliotheek is geïnstalleerd. Als dit niet het geval is, kunt u deze downloaden van de[Aspose.Note voor .NET-documentatie](https://reference.aspose.com/note/net/).
- Ontwikkelomgeving: Zorg ervoor dat er een werkende ontwikkelomgeving, bij voorkeur Microsoft Visual Studio, op uw computer is geïnstalleerd.
- Basiskennis van C#: Maak uzelf vertrouwd met C#, aangezien deze tutorial in deze taal is geschreven.
## Naamruimten importeren
Om te kunnen communiceren met Aspose.Note voor .NET, moet u de benodigde naamruimten in uw project importeren. Voeg de volgende naamruimten toe aan het begin van uw code:
```csharp
using System;
using System.Globalization;
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
```
Laten we nu het proces van het ophalen van lijsten met opsommingstekens of nummering stap voor stap opsplitsen:
## Stap 1: Stel uw documentmap in
```csharp
// Het pad naar de documentenmap.
string dataDir = "Your Document Directory";
```
 Vervangen`"Your Document Directory"` met het daadwerkelijke pad waar uw Aspose.Note-document zich bevindt.
## Stap 2: Laad het document
```csharp
// Laad het document in Aspose.Note.
Document oneFile = new Document(dataDir + "ApplyNumberingOnText.one");
```
 Zorg ervoor dat u vervangt`"ApplyNumberingOnText.one"` met de naam van uw specifieke OneNote-document.
## Stap 3: Verzameling van knooppunten ophalen
```csharp
// Haal een verzameling knooppunten van het overzichtselement op.
IList<OutlineElement> nodes = oneFile.GetChildNodes<OutlineElement>();
```
Met deze stap wordt een verzameling overzichtsknooppunten uit het geladen document opgehaald.
## Stap 4: Herhaal elk knooppunt
```csharp
// Herhaal elk knooppunt.
foreach (OutlineElement node in nodes)
{
    if (node.NumberList != null)
    {
        NumberList list = node.NumberList;
        // Ga door naar de volgende stappen...
    }
}
```
Deze lus zorgt ervoor dat we alleen te maken hebben met knooppunten die een getallenlijst bevatten.
## Stap 5: Lettertype-informatie ophalen
```csharp
// Lettertypenaam ophalen
Console.WriteLine("Font Name: " + list.Font);
// Lettertypelengte ophalen
Console.WriteLine("Font Length: " + list.Font.Length);
// Lettergrootte ophalen
Console.WriteLine("Font Size: " + list.FontSize);
// Letterkleur ophalen
Console.WriteLine("Font Color: " + list.FontColor);
// Formaat ophalen
Console.WriteLine("Font format: " + list.Format);
// Vink vetgedrukt aan
Console.WriteLine("Is bold: " + list.IsBold);
// Controleer cursief
Console.WriteLine("Is italic: " + list.IsItalic);
Console.WriteLine();
```
Deze coderegels halen verschillende lettertypegerelateerde informatie uit de nummerlijst.
## Conclusie
 Gefeliciteerd! U hebt met succes geleerd hoe u lijsten met opsommingstekens of getallen kunt ophalen met Aspose.Note voor .NET. Terwijl u uw verkenning voortzet, raadpleegt u de[documentatie](https://reference.aspose.com/note/net/) voor meer diepgaande inzichten en functionaliteiten.
## Veelgestelde vragen
### Kan ik Aspose.Note voor .NET gebruiken met andere programmeertalen?
Aspose.Note ondersteunt voornamelijk .NET, maar er zijn andere versies van de bibliotheek die zijn afgestemd op verschillende platforms en talen.
### Is Aspose.Note compatibel met de nieuwste OneNote-formaten?
Ja, Aspose.Note ondersteunt een breed scala aan OneNote-indelingen, waardoor compatibiliteit met de nieuwste versies wordt gegarandeerd.
### Hoe kan ik een tijdelijke licentie voor Aspose.Note verkrijgen?
 Bezoek[deze link](https://purchase.aspose.com/temporary-license/) om een tijdelijke licentie te verkrijgen voor evaluatiedoeleinden.
### Welke ondersteuningsopties zijn beschikbaar voor Aspose.Note-gebruikers?
 kunt de omgeving verkennen en hulp zoeken[Aspose.Note-forum](https://forum.aspose.com/c/note/28) voor eventuele vragen of problemen die u tegenkomt.
### Bestaat er een gratis proefversie van Aspose.Note voor .NET?
 Ja, u heeft toegang tot de gratis proefversie van Aspose.Note voor .NET[hier](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
