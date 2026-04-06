---
date: 2026-04-06
description: Leer hoe u een OneNote‑document maakt en een afbeelding programmatically
  invoegt met Aspose.Note voor .NET. Volg eenvoudige stappen om afbeeldingen toe te
  voegen, de uitlijning in te stellen en meer.
keywords:
- create onenote document
- how to insert image
- insert image onenote
- set image alignment
- multiple images onenote
linktitle: Document bouwen en afbeelding invoegen in Aspose.Note
second_title: Aspose.Note .NET API
title: Maak OneNote-document en voeg afbeelding in met Aspose.Note
url: /nl/net/images/build-doc-insert-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak OneNote-document en voeg afbeelding in met Aspose.Note

## Inleiding

In deze tutorial **maak je een OneNote-document** en leer je **hoe je een afbeelding** erin kunt invoegen met Aspose.Note voor .NET. Aspose.Note geeft je volledige controle over OneNote-bestanden, waardoor het eenvoudig is om rijke inhoud zoals afbeeldingen, tabellen en aangepaste lay-outs programmatisch toe te voegen.

## Snelle antwoorden
- **Wat is het primaire doel?** Om een OneNote-document te maken en een afbeelding met aangepaste uitlijning in te voegen.  
- **Welke bibliotheek is vereist?** Aspose.Note voor .NET (download [here](https://releases.aspose.com/note/net/)).  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een betaalde licentie is vereist voor productie.  
- **Kan ik meerdere afbeeldingen toevoegen?** Ja – herhaal de invoegstappen voor elke afbeelding (zie “multiple images onenote” tip).  
- **Wordt PDF-conversie ondersteund?** Absoluut – je kunt later het OneNote-document naar PDF converteren met de `Save`‑methode van Aspose.Note met het PDF‑formaat.

## Vereisten

Voordat we beginnen, zorg ervoor dat je de volgende vereisten hebt:

1. **Visual Studio** – een volledig uitgeruste IDE voor .NET-ontwikkeling.  
2. **Aspose.Note for .NET** – download en installeer de bibliotheek van de officiële site.  
3. **Basic Understanding of C#** – bekendheid met C#-syntaxis helpt je de code‑voorbeelden te volgen.

## Namespaces importeren

Laten we beginnen met het importeren van de benodigde namespaces in je C#-project. Deze namespaces bevatten klassen en methoden die we zullen gebruiken om documentbewerkings‑taken uit te voeren.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Laten we nu het proces van het bouwen van een document en het invoegen van een afbeelding in meerdere stappen opsplitsen:

## Stap 1: Documentobject maken

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document();
```

Deze regel code initialiseert een nieuwe instantie van de `Document`‑klasse, die een OneNote-document vertegenwoordigt.

## Stap 2: Paginaobject initialiseren

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

Hier initialiseren we een nieuwe instantie van de `Page`‑klasse, die een pagina binnen het OneNote-document vertegenwoordigt.

## Stap 3: Outline‑object initialiseren

```csharp
Outline outline = new Outline(doc);
```

De `Outline`‑klasse vertegenwoordigt een outline‑knooppunt in de documenthiërarchie. We maken een nieuw outline‑object om ons document te structureren.

## Stap 4: OutlineElement‑object initialiseren

```csharp
OutlineElement outlineElem = new OutlineElement(doc);
```

Een `OutlineElement` vertegenwoordigt een element binnen een outline. Hier maken we een nieuw outline‑element om inhoud aan ons document toe te voegen.

## Stap 5: Afbeelding laden

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg");
```

We laden een afbeeldingsbestand van het opgegeven pad met behulp van de constructor van de `Image`‑klasse.

## Stap 6: Afbeeldingsuitlijning instellen

```csharp
image.Alignment = HorizontalAlignment.Right;
```

Deze regel stelt de **afbeeldingsuitlijning** in op de rechterkant van de pagina. Je kunt ook `Left` of `Center` kiezen, afhankelijk van je lay-outbehoeften.

## Stap 7: Afbeelding toevoegen aan OutlineElement

```csharp
outlineElem.AppendChildLast(image);
```

Hier voegen we de afbeelding toe aan het outline‑element, waardoor deze in de documentstructuur wordt geplaatst.

## Stap 8: Outline‑element toevoegen aan Outline

```csharp
outline.AppendChildLast(outlineElem);
```

We voegen het outline‑element, samen met de ingevoegde afbeelding, toe aan de outline‑structuur van het document.

## Stap 9: Outline toevoegen aan Pagina

```csharp
page.AppendChildLast(outline);
```

De outline, met de afbeelding, wordt toegevoegd aan de paginastuctuur van het document.

## Stap 10: Pagina toevoegen aan Document

```csharp
doc.AppendChildLast(page);
```

Tot slot voegen we de pagina, compleet met zijn inhoud, toe aan het document.

## Stap 11: Document opslaan

```csharp
dataDir = dataDir + "BuildDocAndInsertImage_out.one";
doc.Save(dataDir);
```

Deze regel slaat het gewijzigde OneNote-document op op de opgegeven locatie. Je kunt later **OneNote PDF converteren** door `doc.Save("output.pdf")` aan te roepen.

## Waarom dit belangrijk is

- **Automation** – Programma‑matig OneNote‑documenten maken bespaart tijd vergeleken met handmatig bewerken.  
- **Consistency** – Met code zorg je ervoor dat elk document dezelfde lay-out- en stijlnormen volgt.  
- **Scalability** – Dezelfde aanpak kan worden uitgebreid om **multiple images onenote**‑documenten in te voegen of rapporten in bulk te genereren.

## Veelvoorkomende valkuilen & tips

- **Path Issues** – Controleer altijd dat `dataDir` naar een geldige map wijst; anders mislukt het laden van de afbeelding.  
- **Image Size** – Grote afbeeldingen kunnen de bestandsgrootte aanzienlijk verhogen; overweeg ze te verkleinen vóór het invoegen.  
- **Multiple Images** – Om meer dan één afbeelding toe te voegen, herhaal Stap 5‑7 voor elke afbeelding en voeg elke toe aan hetzelfde of een ander `OutlineElement`.

## Veelgestelde vragen

### V1: Kan ik meerdere afbeeldingen in één document invoegen met Aspose.Note voor .NET?

A1: Absoluut! Je kunt zoveel afbeeldingen invoegen als je nodig hebt in een document door dezelfde invoegstappen voor elke afbeelding te volgen.

### V2: Ondersteunt Aspose.Note andere bestandsformaten naast OneNote?

A2: Ja, Aspose.Note biedt uitgebreide ondersteuning voor diverse bestandsformaten, waaronder PDF, DOCX, HTML en meer.

### V3: Is Aspose.Note geschikt voor enterprise‑level documentmanagementoplossingen?

A3: Zeker! Aspose.Note biedt robuuste functies en uitstekende prestaties, waardoor het een ideale keuze is voor enterprise‑documentmanagement.

### V4: Kan ik het uiterlijk van ingevoegde afbeeldingen in het document aanpassen?

A4: Ja, Aspose.Note biedt uitgebreide opties voor het aanpassen van het uiterlijk van afbeeldingen, inclusief uitlijning, grootte en rotatie.

### V5: Waar kan ik extra bronnen en ondersteuning vinden voor Aspose.Note voor .NET?

A5: Je kunt de Aspose.Note‑documentatie bekijken [hier](https://reference.aspose.com/note/net/) en hulp zoeken op het Aspose‑communityforum [hier](https://forum.aspose.com/c/note/28/).

---

**Laatst bijgewerkt:** 2026-04-06  
**Getest met:** Aspose.Note 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}