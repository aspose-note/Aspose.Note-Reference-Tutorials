---
title: Stel tabellen samen met Aspose.Note
linktitle: Stel tabellen samen met Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u gestructureerde tabellen met rich-text-inhoud samenstelt met Aspose.Note voor .NET. Verbeter moeiteloos de organisatie en leesbaarheid van documenten.
weight: 11
url: /nl/net/table-manipulation/compose-tables/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stel tabellen samen met Aspose.Note

## Invoering

Tabellen zijn fundamentele componenten van documenten en maken een gestructureerde presentatie van informatie mogelijk. Aspose.Note voor .NET biedt robuuste tools om moeiteloos tabellen samen te stellen. In deze zelfstudie begeleiden we u bij het maken van tabellen met RTF-inhoud met behulp van Aspose.Note.

## Vereisten

Voordat u in de tabelsamenstelling duikt met Aspose.Note voor .NET, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1. Omgevingsconfiguratie: Zorg ervoor dat u een geschikte ontwikkelomgeving hebt ingesteld met .NET Framework of .NET Core.
2.  Installatie: Download en installeer Aspose.Note voor .NET vanaf de[website](https://releases.aspose.com/note/net/).
3. Basiskennis: maak uzelf vertrouwd met de basisconcepten van programmeren in C# en documentmanipulatie.

## Naamruimten importeren

Voordat u tabellen gaat samenstellen, moet u ervoor zorgen dat u de benodigde naamruimten importeert:

```csharp
using System;
using System.Drawing;
using System.IO;
using System.Linq;
```

Laten we het gegeven voorbeeld opsplitsen in beheersbare stappen:

## Stap 1: Stel de documentmap in

Voordat u de tabel samenstelt, definieert u de map waarin het document zal worden opgeslagen.

```csharp
string dataDir = "Your Document Directory";
```

## Stap 2: Maak koptekst

Definieer de koptekst met specifieke stijlen, zoals lettergrootte en vetheid.

```csharp
var headerText = new RichText() { ParagraphStyle = new ParagraphStyle() { FontSize = 18, IsBold = true }, Alignment = HorizontalAlignment.Center }
					.Append("Super contest for suppliers.");
```

## Stap 3: Pagina en overzicht maken

Initialiseer een pagina en een overzicht om de inhoud te structureren.

```csharp
var page = new Page();
var outline = page.AppendChildLast(new Outline() { HorizontalOffset = 50 });
outline.AppendChildLast(new OutlineElement()).AppendChildLast(headerText);
```

## Stap 4: Samenvattingstekst toevoegen

Voeg vóór de tabel een samenvattende tekst toe.

```csharp
var bodyTextHeader = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
bodyTextHeader.Append("This is the final ranking of proposals got from our suppliers.");
```

## Stap 5: Tabel maken

Initialiseer een tabel om gegevens in rijen en kolommen te ordenen.

```csharp
var ranking = outline.AppendChildLast(new OutlineElement()).AppendChildLast(new Table());
```

## Stap 6: Voeg koprij toe

Vul de tabel met een koprij met kolomtitels.

```csharp
var headerRow = ranking.AppendChildFirst(new TableRow());
foreach (var header in new[] { "Supplier", "Contacts", "Score A", "Score B", "Score C", "Final score", "Attached materials", "Comments" })
{
   ranking.Columns.Add(new TableColumn());
   headerRow.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
			 .AppendChildLast(new OutlineElement())
			 .AppendChildLast(new RichText() { ParagraphStyle = headerStyle })
			 .Append(header);
}
```

## Stap 7: lege rijen toevoegen

Voeg lege rijen in ter voorbereiding op het invoegen van gegevens.

```csharp
for (int i = 0; i < 5; i++)
{
   backGroundColor = backGroundColor.IsEmpty ? Color.LightGray : Color.Empty;
   var row = ranking.AppendChildLast(new TableRow());
   for (int j = 0; j < ranking.Columns.Count(); j++)
   {
	   row.AppendChildLast(new TableCell() { BackgroundColor = backGroundColor })
		  .AppendChildLast(new OutlineElement())
		  .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default });
   }
}
```

## Stap 8: Contactgegevens toevoegen

Vul de kolom 'Contacten' in met sjablooninhoud.

```csharp
foreach (var row in ranking.Skip(1))
{
   var contactsCell = row.ElementAt(1);
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("Web: ").Append("link", new TextStyle() { HyperlinkAddress = "www.link.com", IsHyperlink = true });
   contactsCell.AppendChildLast(new OutlineElement())
			   .AppendChildLast(new RichText() { ParagraphStyle = ParagraphStyle.Default })
			   .Append("E-mail: ").Append("mail", new TextStyle() { HyperlinkAddress = "mailto:hi@link.com", IsHyperlink = true });
}
```

## Stap 9: Sla het document op

Sla het samengestelde tabeldocument op.

```csharp
var d = new Document();
d.AppendChildLast(page);
d.Save(Path.Combine(dataDir, "ComposeTable_out.one"));
```

## Stap 10: Bevestiging

Bevestig de succesvolle documentsamenstelling.

```csharp
Console.WriteLine("\nThe document is composed successfully.");
```

## Conclusie

In deze zelfstudie hebben we onderzocht hoe u tabellen met RTF-inhoud kunt samenstellen met behulp van Aspose.Note voor .NET. Door deze stapsgewijze instructies te volgen, kunt u efficiënt gestructureerde tabellen in uw documenten maken, waardoor de leesbaarheid en organisatie wordt verbeterd.

## Veelgestelde vragen

### V1: Kan ik de stijl van tafelelementen aanpassen?
   
A1: Ja, u kunt verschillende aspecten, zoals lettergrootte, kleur en uitlijning, aanpassen aan uw wensen.

### V2: Is Aspose.Note compatibel met andere .NET-bibliotheken?
   
A2: Aspose.Note integreert naadloos met andere .NET-bibliotheken en biedt uitgebreide flexibiliteit bij documentmanipulatie.

### V3: Ondersteunt Aspose.Note het exporteren van tabellen naar verschillende formaten?
   
A3: Absoluut, met Aspose.Note kunt u tabellen exporteren naar verschillende formaten, waaronder PDF, DOCX en HTML.

### V4: Kan ik tabellen dynamisch vullen met gegevens uit externe bronnen?
   
A4: Ja, u kunt tabellen dynamisch vullen door gegevens op te halen uit databases, API's of gebruikersinvoer.

### V5: Is er technische ondersteuning beschikbaar voor Aspose.Note-gebruikers?
   
A5: Ja, Aspose biedt uitgebreide technische ondersteuning via hun forums en speciale ondersteuningskanalen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
