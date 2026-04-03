---
date: 2026-04-03
description: Leer hoe u een hyperlink toevoegt aan Aspose.Note‑documenten met Aspose.Note
  voor .NET, het uiterlijk van hyperlinks aanpast en meerdere hyperlinks invoegt voor
  rijkere OneNote‑bestanden.
keywords:
- how to add hyperlink
- insert multiple hyperlinks
- add hyperlink to onenote
- customize hyperlink appearance
- generate one file hyperlink
linktitle: Hoe een hyperlink toe te voegen in Aspose.Note‑documenten
second_title: Aspose.Note .NET API
title: Hoe een hyperlink toe te voegen aan Aspose.Note‑documenten
url: /nl/net/hyperlinks/add-hyperlinks/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een hyperlink toe te voegen in Aspose.Note-documenten

## Introductie

In deze tutorial ontdek je **hoe je een hyperlink** kunt toevoegen aan tekst in Aspose.Note-documenten met de .NET API. Het toevoegen van een hyperlink verandert statische notities in interactieve, klikbare inhoud—perfect om te linken naar webbronnen, interne secties of externe bestanden. We lopen elke stap door, laten je zien hoe je de **uiterlijk van de hyperlink kunt aanpassen**, en leggen uit hoe je **meerdere hyperlinks kunt invoegen** wanneer je rijkere OneNote-pagina's nodig hebt.

## Snelle antwoorden
- **Wat is de primaire klasse voor het maken van een OneNote‑bestand?** `Document` van Aspose.Note.
- **Welke eigenschap zorgt ervoor dat tekst zich gedraagt als een hyperlink?** `IsHyperlink = true` op `TextStyle`.
- **Kan ik linken naar externe websites?** Ja, stel `HyperlinkAddress` in op een URL zoals `https://www.google.com`.
- **Heb ik een licentie nodig voor productiegebruik?** Een geldige Aspose.Note‑licentie is vereist voor niet‑evaluatie‑builds.
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.

## Wat betekent “hoe een hyperlink toe te voegen” in Aspose.Note?
Een hyperlink toevoegen betekent een URL koppelen aan een stuk tekst zodat, wanneer een gebruiker erop klikt in OneNote, de gekoppelde bron wordt geopend in een browser of een andere applicatie. Aspose.Note biedt de `TextStyle.IsHyperlink`‑vlag en de `HyperlinkAddress`‑eigenschap om dit programmatisch mogelijk te maken.

## Waarom hyperlinks toevoegen aan OneNote‑documenten?
- **Verbeterde navigatie:** Spring direct naar gerelateerde webpagina's of secties.
- **Verbeterde documentatie:** Bied referenties, tutorials of bronbestanden zonder de notitie te verlaten.
- **Professionele uitstraling:** Aanpasbare kleuren en stijlen laten hyperlinks opgaan in het ontwerp van je document.

## Voorwaarden

1. Basiskennis van C# en Visual Studio.
2. Aspose.Note voor .NET‑bibliotheek geïnstalleerd – download deze van [here](https://releases.aspose.com/note/net/).
3. Begrip van de Aspose.Note‑documentstructuur (pagina's, outlines, rich text).

## Namespaces importeren

Importeer eerst de namespaces die je toegang geven tot de kernklassen van Aspose.Note en basis‑.NET‑typen.

```csharp
using System;
using System.Drawing;
```

## Stapsgewijze handleiding

### Stap 1: Maak een nieuw Document‑object

Instantieer een `Document` die al je pagina's en inhoud zal bevatten.

```csharp
Document doc = new Document();
```

### Stap 2: Definieer tekststijlen (inclusief hyperlink‑stijl)

Maak twee `TextStyle`‑objecten – één voor gewone tekst en één voor de hyperlink.  
Hier passen we ook de **uiterlijk van de hyperlink** aan door de letterkleur in te stellen.

```csharp
TextStyle textStyleRed = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

TextStyle textStyleHyperlink = new TextStyle
{
    IsHyperlink = true,
    HyperlinkAddress = "www.google.com"
};
```

> **Pro tip:** Om **meerdere hyperlinks** in te voegen, definieer extra `TextStyle`‑objecten met verschillende `HyperlinkAddress`‑waarden en hergebruik ze in latere `RichText`‑segmenten.

### Stap 3: Maak RichText‑objecten

Bouw de alinea die gewone tekst en de hyperlink combineert. De `Append`‑methode laat je gestileerde fragmenten aan elkaar koppelen.

```csharp
RichText text = new RichText() { ParagraphStyle = ParagraphStyle.Default }
                    .Append("This is ", textStyleRed)
                    .Append("hyperlink", textStyleHyperlink)
                    .Append(". This text is not a hyperlink.", TextStyle.Default);
```

### Stap 4: Maak Outline en Outline‑element

Outlines fungeren als containers voor visuele elementen op een pagina. Stel grootte en positie in naar behoefte.

```csharp
Outline outline = new Outline()
{
    MaxWidth = 200,
    MaxHeight = 200,
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
outlineElem.AppendChildLast(text);
```

### Stap 5: Voeg elementen toe aan een pagina

Elk OneNote‑bestand bestaat uit pagina's. We maken een `Title` en een `Page`, en voegen vervolgens de outline toe.

```csharp
Title title = new Title() { TitleText = titleText };
Page page = new Note.Page() { Title = title };

page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

### Stap 6: Sla het document op

Kies een map, stel de volledige bestandsnaam samen, en roep `Save` aan. Het uitvoerbestand wordt een geldig OneNote `.one`‑bestand dat je hyperlink bevat.

```csharp
string dataDir = "Your Document Directory";
string outputFilePath = Path.Combine(dataDir, "AddHyperlink_out.one");
doc.Save(outputFilePath);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| Hyperlink opent niet | Zorg ervoor dat `HyperlinkAddress` het protocol bevat (`http://` of `https://`). |
| Tekstkleur wordt niet toegepast | Stel `FontColor` in op de `TextStyle` die voor de hyperlink wordt gebruikt. |
| Meerdere links op één pagina nodig | Maak meerdere `TextStyle`‑objecten, elk met een eigen `HyperlinkAddress`, en voeg ze toe aan dezelfde of verschillende `RichText`‑objecten. |
| Document laadt niet in OneNote | Controleer of je een ondersteunde OneNote‑versie gebruikt (2010+). |

## Veelgestelde vragen

**Q: Kan ik meerdere hyperlinks binnen hetzelfde document toevoegen met Aspose.Note?**  
A: Ja, maak eenvoudig extra `TextStyle`‑instanties met verschillende `HyperlinkAddress`‑waarden en voeg ze toe aan je `RichText`‑objecten.

**Q: Hoe kan ik de uitstraling van hyperlinks aanpassen?**  
A: Gebruik eigenschappen zoals `FontColor`, `FontName` en `FontSize` op de `TextStyle` met `IsHyperlink = true`. Hiermee kun je de branding van je document volgen.

**Q: Ondersteunt Aspose.Note hyperlinks naar externe websites?**  
A: Absoluut. Stel `HyperlinkAddress` in op een geldige URL (inclusief `http://` of `https://`) om te linken vanuit het OneNote‑bestand.

**Q: Is het mogelijk om één OneNote‑bestand te genereren dat veel hyperlinks bevat?**  
A: Ja. Door herhaaldelijk gestileerde `RichText`‑segmenten met verschillende hyperlink‑adressen toe te voegen, kun je een **collectie van hyperlinks in één bestand** genereren.

**Q: Is Aspose.Note compatibel met de nieuwste OneNote‑versies?**  
A: De bibliotheek werkt met OneNote 2010 en later, inclusief de Windows 10 UWP‑versie.

---

**Laatste update:** 2026-04-03  
**Getest met:** Aspose.Note for .NET 24.11  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}