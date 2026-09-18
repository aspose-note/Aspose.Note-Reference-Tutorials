---
date: 2026-05-05
description: Leer hoe je een afbeelding in Aspose.Note‑documenten kunt invoegen met
  .NET. Deze stapsgewijze gids laat zien hoe je een afbeelding kunt uitlijnen, een
  afbeelding aan een pagina kunt toevoegen en visuele inhoud kunt verbeteren.
keywords:
- how to insert image
- how to align image
- append image to page
linktitle: Afbeeldingen invoegen in Aspose.Note‑documenten
second_title: Aspose.Note .NET API
title: Hoe een afbeelding in Aspose.Note-documenten in te voegen met .NET
url: /nl/net/images/insert-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een afbeelding in Aspose.Note-documenten in te voegen met .NET

## Introductie

Als je je Aspose.Note‑bestanden aantrekkelijker wilt maken, **hoe een afbeelding in te voegen** is de eerste vaardigheid die je wilt beheersen. In deze tutorial lopen we de exacte stappen door die je nodig hebt om afbeeldingen toe te voegen, hun grootte te regelen, ze nauwkeurig te positioneren en zelfs uit te lijnen zoals je wilt. Aan het einde kun je gemakkelijk afbeeldingen invoegen, uitlijnen en een afbeelding aan een pagina toevoegen — allemaal met schone, leesbare C#‑code.

## Snelle antwoorden
- **Welke bibliotheek is vereist?** Aspose.Note for .NET  
- **Kan ik de afbeeldingsgrootte programmatically instellen?** Ja – gebruik de Width en Height‑eigenschappen.  
- **Hoe positioneer ik een afbeelding?** Pas HorizontalOffset, VerticalOffset aan of gebruik uitlijnopties.  
- **Is er een limiet op afbeeldingsformaten?** JPG, PNG, BMP, GIF en andere worden ondersteund.  
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.Note‑licentie is vereist voor commercieel gebruik.

## Wat is het invoegen van een afbeelding in Aspose.Note?

Een afbeelding invoegen betekent het maken van een Aspose.Note.Image‑object, het configureren van de visuele eigenschappen, en het toevoegen aan een pagina in een OneNote‑compatibel .one‑bestand. Hiermee kun je notities verrijken met screenshots, diagrammen of andere visuele hulpmiddelen.

## Waarom afbeeldingen invoegen met Aspose.Note?

- **Betere communicatie:** Visuals verduidelijken complexe ideeën sneller dan alleen tekst.  
- **Consistente lay-out:** Programmatic control zorgt ervoor dat elk document dezelfde ontwerpnormen volgt.  
- **Automatisering vriendelijk:** Ideaal voor het genereren van rapporten, tutorials of batch‑verwerkte notitieblokken.

## Vereisten

1. Aspose.Note for .NET: Download en installeer Aspose.Note for .NET vanaf [hier](https://releases.aspose.com/note/net/).  
2. Afbeeldingsbestanden: Zorg dat de afbeeldingsbestanden (JPG, PNG, enz.) die je wilt insluiten klaarstaan op schijf.

## Namespaces importeren

We beginnen met het importeren van de namespaces die ons toegang geven tot bestands‑I/O en de Aspose.Note‑API.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

## Stap 1: Document laden en pagina ophalen

Open eerst het bestaande .one‑document en haal de pagina op waar de afbeelding zal worden geplaatst.

```csharp
string dataDir = "Your Document Directory";
Document doc = new Document(dataDir + "YourDocument.one");
Aspose.Note.Page page = doc.FirstChild;
```

## Hoe een afbeelding uitlijnen

Voordat we de afbeelding toevoegen, bepaal hoe deze moet uitlijnen met andere inhoud. Aspose.Note biedt horizontale uitlijnopties (Links, Midden, Rechts). Je kunt de plaatsing ook fijn afstellen met offset‑waarden.

## Stap 2: Afbeelding laden en eigenschappen instellen

Maak het Image‑object, wijs het naar je bestand, en definieer de afmetingen, offsets en uitlijning.

```csharp
Aspose.Note.Image image = new Aspose.Note.Image(doc, dataDir + "image.jpg")
{
    Width = 100,                // Set image width
    Height = 100,               // Set image height
    HorizontalOffset = 100,     // Set horizontal offset
    VerticalOffset = 400,       // Set vertical offset
    Alignment = HorizontalAlignment.Right  // Set image alignment
};
```

## Afbeelding aan pagina toevoegen

Nu de afbeelding volledig is geconfigureerd, voeg je deze toe aan de elementboom van de pagina.

```csharp
page.AppendChildLast(image);
```

## Veelvoorkomende valkuilen & tips

- **Onjuiste offsets:** Onthoud dat offsets worden gemeten vanaf de linkerbovenhoek van de pagina. Een grote verticale offset kan de afbeelding buiten het scherm duwen.  
- **Niet‑ondersteund formaat:** Als je een formaat probeert dat niet wordt herkend, zal Aspose.Note een uitzondering werpen — converteer het bestand eerst naar JPG of PNG.  
- **Licentie‑waarschuwingen:** Werken zonder licentie voegt een watermerk toe aan het gegenereerde document; pas altijd je licentie toe in productie.

## Conclusie

Je hebt nu geleerd **hoe een afbeelding in te voegen** in een Aspose.Note‑document, hoe **een afbeelding uit te lijnen**, en hoe **een afbeelding aan een pagina toe te voegen** met een paar eenvoudige regels C#. Deze technieken stellen je in staat om automatisch rijkere, professionelere notitieblokken te bouwen.

## Veelgestelde vragen

### Q1: Kan ik afbeeldingen van elk formaat in Aspose.Note‑documenten invoegen?

A1: Ja, Aspose.Note ondersteunt verschillende afbeeldingsformaten, waaronder JPG, PNG, BMP, GIF, enz.

### Q2: Is het mogelijk om de ingevoegde afbeeldingen programmatically te schalen?

A2: Absoluut! Je kunt de breedte en hoogte van afbeeldingen aanpassen aan je voorkeuren tijdens het invoegen.

### Q3: Biedt Aspose.Note opties om de uitlijning van afbeeldingen aan te passen?

A3: Ja, je kunt afbeeldingen uitlijnen naar links, rechts of midden binnen de pagina's van je document.

### Q4: Kan ik meerdere afbeeldingen in één pagina van mijn document invoegen?

A4: Zeker! Je kunt zoveel afbeeldingen invoegen als je nodig hebt op één pagina met behulp van Aspose.Note.

### Q5: Is er een limiet aan de bestandsgrootte van afbeeldingen die kunnen worden ingevoegd?

A5: Aspose.Note legt geen strikte beperkingen op aan de bestandsgrootte van afbeeldingen, maar het wordt aanbevolen om afbeeldingen te optimaliseren voor betere prestaties.

## Veelgestelde vragen

**Q: Hoe laad ik een afbeelding vanuit een stream in plaats van een bestandspad?**  
A: Gebruik de Image(Stream, Document)‑constructor en geef een MemoryStream mee die de afbeeldingsbytes bevat.

**Q: Kan ik de afbeelding wijzigen nadat deze aan de pagina is toegevoegd?**  
A: Ja, je kunt de Width, Height, HorizontalOffset, VerticalOffset, en Alignment‑eigenschappen van het bestaande Image‑object aanpassen en vervolgens page.Update() aanroepen.

**Q: Is het mogelijk om een bijschrift onder de afbeelding toe te voegen?**  
A: Voeg een RichText‑element toe na de afbeelding en stel de tekst in als bijschrift.

**Q: Ondersteunt Aspose.Note geanimeerde GIF's?**  
A: Geanimeerde GIF's worden behandeld als statische afbeeldingen; alleen het eerste frame wordt weergegeven.

**Q: Wat moet ik doen als de afbeelding onscherp lijkt?**  
A: Zorg ervoor dat de bronafbeelding voldoende resolutie heeft en vermijd het opschalen boven de oorspronkelijke grootte.

---

**Laatst bijgewerkt:** 2026-05-05  
**Getest met:** Aspose.Note 23.12 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}