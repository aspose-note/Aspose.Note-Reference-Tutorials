---
title: Genereer een document uit de sjabloon in Aspose.Note
linktitle: Genereer een document uit de sjabloon in Aspose.Note
second_title: Aspose.Note .NET API
description: Genereer moeiteloos dynamische documenten met Aspose.Note voor .NET. Volg onze stapsgewijze handleiding voor gepersonaliseerde en datagestuurde documentcreatie.
weight: 18
url: /nl/net/text-manipulation/generate-document-from-template/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Genereer een document uit de sjabloon in Aspose.Note

## Invoering
In het steeds evoluerende landschap van documentcreatie onderscheidt Aspose.Note voor .NET zich als een krachtig hulpmiddel voor het moeiteloos genereren van dynamische documenten. Of u nu te maken heeft met rapporten, facturen of gepersonaliseerde documenten, deze tutorial leidt u door het proces van het genereren van een document op basis van een sjabloon met behulp van Aspose.Note voor .NET.
## Vereisten
Voordat u in de stapsgewijze handleiding duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:
1.  Aspose.Note voor .NET-bibliotheek: Download en installeer de bibliotheek vanaf de .NET-bibliotheek[Aspose.Note voor .NET-documentatie](https://reference.aspose.com/note/net/).
2. Documentsjabloon: bereid een sjabloondocument voor in de OneNote-indeling (met de extensie .one). Dit zal dienen als de basis voor uw dynamisch gegenereerde document.
## Naamruimten importeren
Zorg ervoor dat u de benodigde naamruimten in uw project opneemt:
```csharp
    using System;
    using System.Collections.Generic;
    using System.IO;
```
Laten we nu elke stap in de handleiding opsplitsen.
## Stap 1: Definieer uw documentenmap
```csharp
string dataDir = "Your Document Directory";
```
Vervang "Uw documentenmap" door het pad waar u uw gegenereerde document wilt opslaan.
## Stap 2: Maak een woordenboek met vervangende waarden
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
Definieer een woordenboek waarbij de sleutels tijdelijke aanduidingen zijn in uw sjabloon, en waarden de gegevens zijn waarmee u ze wilt vervangen.

## Stap 3: Laad het sjabloondocument
```csharp
var templateDocument = new Document(Path.Combine(dataDir, "JobOffer.one"));
```
Laad uw OneNote-sjabloondocument in Aspose.Note.

## Stap 4: Vervang sjabloonwoorden door dynamische gegevens
```csharp
foreach (var paragraph in templateDocument.GetChildNodes<RichText>())
{
    foreach (var replacement in templateData)
    {
        paragraph.Replace($"${{{replacement.Key}}}", replacement.Value);
    }
}
```
Herhaal elke alinea in de sjabloon en vervang tijdelijke aanduidingen door dynamische gegevens.

## Stap 5: Sla het gegenereerde document op
```csharp
templateDocument.Save(Path.Combine(dataDir, "JobOffer_out.one"));
```
Sla het dynamisch gegenereerde document op in de door u opgegeven map.

## Conclusie
Gefeliciteerd! U hebt met succes een dynamisch document gegenereerd met Aspose.Note voor .NET. Dit proces opent een wereld aan mogelijkheden voor het naadloos creëren van gepersonaliseerde en datagestuurde documenten.

## Veel Gestelde Vragen
### Kan ik Aspose.Note voor .NET gebruiken met andere documentformaten?
Ja, Aspose.Note voor .NET houdt zich voornamelijk bezig met OneNote-documenten, maar Aspose biedt verschillende bibliotheken voor verschillende formaten.
### Is er een gratis proefversie beschikbaar voor Aspose.Note voor .NET?
Ja, u kunt de mogelijkheden van Aspose.Note voor .NET verkennen met een gratis proefperiode. Bezoek[hier](https://releases.aspose.com/) voor meer informatie.
### Hoe kan ik ondersteuning krijgen voor Aspose.Note voor .NET?
 Bezoek de[Aspose.Note voor .NET-forum](https://forum.aspose.com/c/note/28) om hulp te krijgen van de gemeenschap en experts.
### Zijn er tijdelijke licenties beschikbaar voor Aspose.Note voor .NET?
 Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/) voor test- en evaluatiedoeleinden.
### Waar kan ik uitgebreide documentatie vinden voor Aspose.Note voor .NET?
 Verwijs naar de[documentatie](https://reference.aspose.com/note/net/) voor uitgebreide informatie over het gebruik van Aspose.Note voor .NET.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
