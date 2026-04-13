---
date: 2026-04-13
description: Leer hoe je afbeeldingen toevoegt aan OneNote‑documenten met behulp van
  afbeeldingsstreams in .NET met Aspose.Note. Deze stapsgewijze gids behandelt het
  laden van afbeeldingen vanuit een stream, het toevoegen ervan aan outlines en het
  opslaan van het bestand.
keywords:
- add image to onenote
- how to insert image
- load image from stream
- append image to outline
- image stream .net
linktitle: Afbeelding toevoegen aan OneNote via afbeeldingstroom met Aspose.Note
second_title: Aspose.Note .NET API
title: Afbeelding toevoegen aan OneNote via afbeeldingsstroom met Aspose.Note
url: /nl/net/images/insert-image-using-image-stream/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding toevoegen aan OneNote via Image Stream met Aspose.Note

## Inleiding

In deze tutorial ontdek je **hoe je een afbeelding aan OneNote** documenten kunt toevoegen door een afbeelding vanuit een stream te laden en deze aan een outline toe te voegen met Aspose.Note voor .NET. Of je nu een rapportagetool, een notitie‑app of automatisering van documentatie bouwt, het programmatically invoegen van afbeeldingen maakt je OneNote‑bestanden veel aantrekkelijker en bruikbaarder.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.Note for .NET (free trial available).  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Kan ik afbeeldingen vanuit een stream laden?** Ja – gebruik `FileStream` of een andere `Stream`‑implementatie.  
- **Hoe regel ik de uitlijning van de afbeelding?** Stel de `Alignment`‑eigenschap in (bijv. `HorizontalAlignment.Right`).  
- **Welk bestandsformaat wordt geproduceerd?** Een OneNote (`.one`) bestand dat geopend kan worden in Microsoft OneNote.

## Wat betekent “afbeelding toevoegen aan OneNote”?

Een afbeelding toevoegen aan een OneNote‑bestand betekent dat je een visueel element direct in de inhoudshiërarchie van een pagina embedde. Met Aspose.Note werk je met objecten zoals `Document`, `Page`, `Outline` en `OutlineElement`. Door een `Image`‑object in een `OutlineElement` te plaatsen, wordt de foto onderdeel van de OneNote‑paginalay‑out.

## Waarom Aspose.Note gebruiken voor het invoegen van afbeeldingen?

- **Geen Office‑installatie vereist** – genereer of wijzig OneNote‑bestanden op een server.  
- **Volledige controle over lay‑out** – uitlijnen, formaat wijzigen en afbeeldingen precies plaatsen waar je ze nodig hebt.  
- **Stream‑vriendelijk** – werkt met elke `Stream`, perfect voor cloudopslag of alleen‑geheugen scenario's.  
- **Cross‑platform** – compatibel met Windows, Linux en macOS .NET runtimes.

## Vereisten

1. **Ontwikkelomgeving** – Visual Studio 2022 of elke .NET‑compatibele IDE.  
2. **Aspose.Note Bibliotheek** – download deze van de officiële site [here](https://releases.aspose.com/note/net/).  
3. **Afbeeldingsbestanden** – ten minste één afbeelding (JPG, PNG, BMP, GIF of TIFF) die je wilt insluiten.  
4. **Basis C#‑kennis** – vertrouwd met bestandsafhandeling en objectgeoriënteerde code.

## Namespaces importeren
Eerst importeren we de namespaces die ons toegang geven tot Aspose.Note‑klassen en standaard .NET I/O‑hulpmiddelen.

```csharp
using System.IO;
using Aspose.Note;
using System.Collections.Generic;
using System.Drawing;
using System;
```

Laten we nu stap voor stap door het proces lopen.

### Stap 1: Documentobject initialiseren
We beginnen met het maken van een nieuw `Document`‑instance dat het OneNote‑bestand zal bevatten.

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
Document doc = new Document();
```

### Stap 2: Pagina‑object maken
Een OneNote‑bestand bestaat uit één of meer pagina's. Hier maken we een nieuwe pagina om onze inhoud te hosten.

```csharp
Aspose.Note.Page page = new Aspose.Note.Page(doc);
```

### Stap 3: Outline‑ en OutlineElement‑objecten initialiseren
Outlines zijn containers voor rijke inhoud (tekst, afbeeldingen, tabellen). Een `OutlineElement` is een kind dat daadwerkelijk de items bevat.

```csharp
Outline outline1 = new Outline(doc);
OutlineElement outlineElem1 = new OutlineElement(doc);
```

### Stap 4: Afbeelding laden vanuit stream
Met een `FileStream` (of een andere `Stream`) lezen we het afbeeldingsbestand en maken we een `Image`‑object. Dit is waar het **load image from stream**‑keyword schittert.

```csharp
using (FileStream fs = File.OpenRead(dataDir + "image.jpg"))
{
    Aspose.Note.Image image1 = new Aspose.Note.Image(doc, "Penguins.jpg", fs)
    {
        Alignment = HorizontalAlignment.Right
    };
    outlineElem1.AppendChildLast(image1);
}
```

### Stap 5: Afbeelding toevoegen aan OutlineElement
De afbeelding maakt nu deel uit van het `OutlineElement`. Deze stap demonstreert de **append image to outline**‑functionaliteit.

```csharp
outlineElem1.AppendChildLast(image1);
```

### Stap 6: OutlineElement toevoegen aan Outline
We voegen nu het element (met de afbeelding) toe aan de outline‑container.

```csharp
outline1.AppendChildLast(outlineElem1);
```

### Stap 7: Outline toevoegen aan pagina
De outline, met de afbeelding, wordt toegevoegd aan de pagina.

```csharp
page.AppendChildLast(outline1);
```

### Stap 8: Pagina toevoegen aan document
Met de pagina klaar, voegen we deze in de documenthiërarchie in.

```csharp
doc.AppendChildLast(page);
```

### Stap 9: Document opslaan
Tot slot slaan we het OneNote‑bestand op schijf op. Het resulterende bestand kan geopend worden in Microsoft OneNote.

```csharp
doc.Save(dataDir + "BuildDocAndInsertImageUsingImageStream_out.one");
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **Afbeelding verschijnt niet** | De stream werd gesloten voordat de afbeelding werd toegevoegd. | Houd het `using`‑blok rond de `AppendChildLast`‑aanroep (zoals getoond). |
| **Onjuiste uitlijning** | `Alignment`‑eigenschap niet ingesteld of later overschreven. | Stel `Alignment` in bij het maken van de `Image` of wijzig `image1.Alignment` vóór het toevoegen. |
| **Niet‑ondersteund afbeeldingsformaat** | Poging een formaat te laden dat niet door Aspose.Note wordt herkend. | Converteer de afbeelding eerst naar JPG, PNG, BMP, GIF of TIFF. |
| **Bestandspad‑fouten** | `dataDir` wijst naar een niet‑bestaande map. | Gebruik `Path.Combine` en controleer of de map bestaat voordat je uitvoert. |

## Veelgestelde vragen

**Q: Kan ik meerdere afbeeldingen in één document invoegen met deze methode?**  
A: Ja. Herhaal simpelweg de *Afbeelding laden vanuit stream* en *Afbeelding toevoegen aan OutlineElement* stappen voor elke afbeelding.

**Q: Ondersteunt Aspose.Note andere afbeeldingsformaten naast JPG?**  
A: Absoluut. PNG, BMP, GIF en TIFF worden allemaal ondersteund.

**Q: Kan ik de uitlijning en grootte van ingevoegde afbeeldingen aanpassen?**  
A: Ja. Naast `Alignment` kun je de `Width`, `Height` en `Scale`‑eigenschappen op het `Image`‑object instellen.

**Q: Is Aspose.Note compatibel met alle versies van .NET?**  
A: Het werkt met .NET Framework 4.5+, .NET Core 3.1+, .NET 5, en .NET 6+.

**Q: Waar kan ik extra bronnen en ondersteuning voor Aspose.Note vinden?**  
A: Je kunt uitgebreide documentatie, forums en support vinden op het [Aspose Forum](https://forum.aspose.com/c/note/28).

---

**Laatst bijgewerkt:** 2026-04-13  
**Getest met:** Aspose.Note 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}