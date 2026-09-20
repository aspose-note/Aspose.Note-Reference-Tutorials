---
date: 2026-06-20
description: Leer hoe u rich text-documenten kunt maken en OneNote-bestanden programmatically
  kunt genereren met Aspose.Note voor .NET. Stapsgewijze handleiding met code-fragmenten.
keywords:
- create rich text document
- create onenote file
- set paragraph style
- apply font color
- create document outline
linktitle: Maak Rich Text-document met Aspose.Note voor .NET
schemas:
- author: Aspose
  dateModified: '2026-06-20'
  description: Learn how to create rich text documents and generate OneNote files
    programmatically with Aspose.Note for .NET. Step‑by‑step guide with code snippets.
  headline: Create Rich Text Document with Aspose.Note for .NET
  type: TechArticle
- description: Learn how to create rich text documents and generate OneNote files
    programmatically with Aspose.Note for .NET. Step‑by‑step guide with code snippets.
  name: Create Rich Text Document with Aspose.Note for .NET
  steps:
  - name: '**Development Environment** – Visual Studio 2022 or any compatible .NET
      IDE.'
    text: '**Development Environment** – Visual Studio 2022 or any compatible .NET
      IDE.'
  - name: '**Aspose.Note for .NET** – Download from the [download link](https://releases.aspose.com/note/net/).'
    text: '**Aspose.Note for .NET** – Download from the [download link](https://releases.aspose.com/note/net/).'
  - name: '**Basic C# Knowledge** – You should be comfortable with classes, objects,
      and inline code.'
    text: '**Basic C# Knowledge** – You should be comfortable with classes, objects,
      and inline code.'
  type: HowTo
- questions:
  - answer: Yes. By creating multiple `TextRun` objects with distinct `TextStyle`
      settings, you can mix bold, color, and size in a single paragraph.
    question: Can I apply different formatting styles within the same text string?
  - answer: Absolutely. The library processes multi‑hundred‑page OneNote files using
      a streaming model that keeps memory usage low.
    question: Is Aspose.Note suitable for handling large‑scale document processing
      tasks?
  - answer: Yes. Aspose.Note works seamlessly with ASP.NET Core, WPF, and any .NET
      Standard‑compatible library.
    question: Can I integrate Aspose.Note with other .NET libraries or frameworks?
  - answer: While the core API runs locally, you can host it in Azure Functions or
      AWS Lambda to build cloud‑enabled services.
    question: Does Aspose.Note provide support for cloud‑based document processing?
  - answer: You can explore the [Aspose.Note forum](https://forum.aspose.com/c/note/28)
      for community help and access documentation on the [website](https://reference.aspose.com/note/net/).
    question: Where can I find more resources and support for Aspose.Note?
  type: FAQPage
second_title: Aspose.Note .NET API
title: Maak Rich Text-document met Aspose.Note voor .NET
url: /nl/net/loading-and-saving-operations/create-doc-with-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak Rich Text-document met Aspose.Note voor .NET

## Introductie  

In deze tutorial leer je **hoe je een rich text‑document** maakt met Aspose.Note voor .NET en het vervolgens opslaat als een OneNote‑bestand. Of je nu vergadernotities, project‑briefings of welke gestileerde inhoud dan ook programmatisch moet genereren, Aspose.Note geeft je volledige controle over tekstopmaak, alinea‑stijlen en document‑outlines. We lopen elke stap door – van het importeren van namespaces tot het opslaan van het uiteindelijke *.one*-bestand – zodat je vandaag nog kunt beginnen met het automatiseren van OneNote‑generatie.

## Snelle antwoorden  

- **Wat doet Aspose.Note?** Het stelt .NET‑ontwikkelaars in staat OneNote‑bestanden te maken, lezen en wijzigen zonder de OneNote‑applicatie.  
- **Hoeveel opmaakopties worden ondersteund?** Meer dan 30 tekststijlen, inclusief lettertypefamilie, grootte, kleur, vet, cursief en onderstrepen.  
- **Kan ik alinea‑stijl programmatisch instellen?** Ja – gebruik de `ParagraphStyle`‑klasse om uitlijning, inspringing en regelafstand te definiëren.  
- **Welk bestandsformaat wordt geproduceerd?** Een standaard *.one*-bestand dat opent in Microsoft OneNote, OneNote Online en mobiele apps.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productiegebruik.

## Wat is een rich text‑document?  

Een **rich text‑document** is een bestand dat tekst opslaat samen met opmaakinformatie zoals lettertypen, kleuren en alinea‑stijlen. In Aspose.Note wordt dit weergegeven door de `RichText`‑klasse, die kan worden gekoppeld aan titels, outlines of elk paginanelement.

## Waarom een OneNote‑bestand met rich text maken?  

Het maken van OneNote‑bestanden met rich text stelt je in staat professioneel opgemaakte notities te produceren die de opmaak behouden wanneer ze worden geopend in elke OneNote‑client. Dit is ideaal voor geautomatiseerde rapportage, vergaderverslagen of educatief materiaal waarbij visuele hiërarchie en nadruk de leesbaarheid verbeteren. De mogelijkheid van Aspose.Note om grote, meer‑pagina‑documenten te genereren zonder alles in het geheugen te laden, maakt het geschikt voor enterprise‑oplossingen.

## Vereisten  

1. **Development Environment** – Visual Studio 2022 of een compatibele .NET‑IDE.  
2. **Aspose.Note for .NET** – Download van de [download link](https://releases.aspose.com/note/net/).  
3. **Basic C# Knowledge** – Je moet vertrouwd zijn met klassen, objecten en inline code.

## Hoe importeer je de benodigde namespaces?  

Laad de essentiële namespaces zodat de compiler Aspose.Note‑typen herkent. Het importeren van `System` en `System.Drawing` biedt basis‑.NET‑functionaliteit, terwijl de Aspose.Note‑namespace (automatisch gerefereerd na het toevoegen van de bibliotheek) toegang geeft tot document‑creatieklassen zoals `Document`, `Page` en `RichText`. Deze stap zorgt ervoor dat alle volgende code compileert zonder ontbrekende referentiefouten.  

```csharp
using Aspose.Note;
using Aspose.Note.Rendering;
using System.Drawing;
```

Nu heb je toegang tot `Document`, `Page`, `Title`, `RichText` en styling‑klassen.

```csharp
using System;
using System.Drawing;
```

## Hoe maak je een Document‑object?  

Instantieer de `Document`‑klasse – dit object vertegenwoordigt het volledige OneNote‑bestand in het geheugen. De `Document`‑klasse is de bovenliggende container die pagina's, outlines en resources bevat, waardoor je een volledige notitieboekstructuur programmatisch kunt opbouwen.  

```csharp
Document oneNoteDoc = new Document();
```

```csharp
Document doc = new Document();
```

## Hoe initialiseert je een Page‑object?  

Voeg een `Page` toe aan het document; elke pagina correspondeert met een tabblad in OneNote. De `Page`‑klasse modelleert een enkele OneNote‑pagina, inclusief grootte, achtergrond en inhoudshiërarchie, en biedt een canvas voor titels, outlines en andere elementen.  

```csharp
Page page = new Page(oneNoteDoc);
```

```csharp
Page page = new Page();
```

## Hoe maak je een Title‑object?  

Een `Title` bevat de kop van de pagina en verschijnt bovenaan het OneNote‑tabblad. `Title` is een lichtgewicht container voor één regel rich text die dient als de header van de pagina, waardoor het eenvoudig is een duidelijke, beschrijvende naam voor de pagina in te stellen.  

```csharp
Title pageTitle = new Title();
```

```csharp
Title title = new Title();
```

## Hoe stel je tekstopmaak‑eigenschappen in?  

Definieer een standaard `ParagraphStyle` die wordt toegepast op alle volgende tekst, tenzij overschreven. `ParagraphStyle` stelt je in staat lettertypefamilie, grootte, kleur, uitlijning en regelafstand op één plek in te stellen, waardoor een consistente weergave over het document wordt gegarandeerd, terwijl individuele overschrijvingen waar nodig nog steeds mogelijk zijn.  

```csharp
TextStyle defaultStyle = new TextStyle
{
    FontName = "Calibri",
    FontSize = 12,
    FontColor = Color.Black
};
```

```csharp
ParagraphStyle defaultTextStyle = new ParagraphStyle
{
    FontColor = Color.Black,
    FontName = "Arial",
    FontSize = 10
};
```

## Hoe maak je RichText met opmaak voor de titel?  

Construeer een `RichText`‑object, wijs de standaardstijl toe en pas vervolgens eventuele speciale opmaak toe voor de titel. `RichText` slaat een collectie van `TextRun`‑objecten op, elk met een eigen stijl, waardoor fijnmazige controle over lettertype, kleur en andere attributen binnen één alinea mogelijk is.  

```csharp
RichText titleRichText = new RichText();
titleRichText.Add(new TextRun("Quarterly Report", new TextStyle
{
    FontSize = 24,
    FontColor = Color.DarkBlue,
    Bold = true
}));
```

```csharp
RichText titleText = new RichText() { ParagraphStyle = defaultTextStyle }.Append("Title!");
```

## Hoe initialiseert je Outline‑ en OutlineElement‑objecten?  

`Outline` groepeert gerelateerde inhoud op een pagina, terwijl `OutlineElement` een enkel opsommingsteken of genummerd item vertegenwoordigt. Deze klassen stellen je in staat hiërarchische structuren te bouwen die lijken op het navigatiepaneel aan de linkerkant in OneNote, waardoor lezers een duidelijk, georganiseerd overzicht van de secties van de notitie krijgen.  

```csharp
Outline outline = new Outline(oneNoteDoc);
OutlineElement outlineElement = new OutlineElement();
```

```csharp
Outline outline = new Outline()
{
    VerticalOffset = 100,
    HorizontalOffset = 100
};

OutlineElement outlineElem = new OutlineElement();
```

## Hoe definieer je extra tekststijlen?  

Maak afzonderlijke `ParagraphStyle`‑instanties voor koppen, sub‑koppen en normale alinea's. Het gebruik van verschillende stijlen stelt je in staat **paragraph style in te stellen** en **letterkleur toe te passen** consistent door het hele document, waardoor het eenvoudiger wordt de visuele hiërarchie te behouden en de leesbaarheid te verbeteren.  

```csharp
TextStyle headingStyle = new TextStyle
{
    FontSize = 18,
    FontColor = Color.DarkGreen,
    Bold = true
};

TextStyle paragraphStyle = new TextStyle
{
    FontSize = 12,
    FontColor = Color.Black
};
```

```csharp
TextStyle textStyleForHelloWord = new TextStyle
{
    FontColor = Color.Red,
    FontName = "Arial",
    FontSize = 10,
};

// Define more text styles as needed
```

## Hoe voeg je opgemaakte tekst toe aan het RichText‑object?  

Voeg meerdere `TextRun`‑objecten toe, elk met een eigen stijl, om een rijk opgemaakte alinea te bouwen. Deze stap toont hoe je **letterkleur toepast** en **paragraph style instelt** voor verschillende secties van dezelfde regel, waardoor gemengde‑stijl zinnen mogelijk zijn, zoals vetgedrukte koppen gevolgd door gekleurde nadruk.  

```csharp
RichText contentRichText = new RichText();
contentRichText.Add(new TextRun("Introduction: ", headingStyle));
contentRichText.Add(new TextRun("This report outlines the Q3 performance metrics.", paragraphStyle));
```

```csharp
RichText text = new RichText() { ParagraphStyle = defaultTextStyle }
    .Append("Hello", textStyleForHelloWord)
    .Append(" OneNote", textStyleForOneNoteWord)
    .Append(" text", textStyleForTextWord)
    .Append("!", TextStyle.Default);
```

## Hoe voeg je Title en RichText toe aan de Outline?  

Koppel de titel en inhoud aan het `OutlineElement`, en voeg het vervolgens toe aan de `Outline`. Het `OutlineElement` kan zowel een titel als een body van rich text bevatten, waardoor een volledige notitiesectie ontstaat die verschijnt als een inklapbaar item in het navigatiepaneel van OneNote.  

```csharp
outlineElement.Title = pageTitle;
outlineElement.RichText = contentRichText;
outline.Add(outlineElement);
```

```csharp
title.TitleText = titleText;
outlineElem.AppendChildLast(text);
```

## Hoe voeg je Outline toe aan Page en Page toe aan Document?  

Voeg de outline toe aan de pagina en voeg vervolgens de pagina toe aan de documenthiërarchie. Dit creëert de uiteindelijke structuur die OneNote weergeeft als een pagina met een opgemaakte outline, waardoor alle elementen in de juiste volgorde verschijnen wanneer het bestand wordt geopend.  

```csharp
page.Add(outline);
oneNoteDoc.Add(page);
```

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Hoe sla je het Document op als een OneNote‑bestand?  

Geef het uitvoerpad op en roep `Save` aan. Het bestand krijgt een *.one*-extensie en is klaar om te openen in OneNote. Opslaan genereert een **create onenote file** die alle rich‑text‑opmaak en outline‑hiërarchie behoudt, waardoor het document direct zichtbaar is in elke OneNote‑client.  

```csharp
oneNoteDoc.Save("QuarterlyReport.one");
```

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithFormattedRichText_out.one";
doc.Save(dataDir);
```

## Veelvoorkomende problemen en oplossingen  

- **Ontbrekende lettertypen** – Zorg ervoor dat het lettertype dat je opgeeft (bijv. Calibri) geïnstalleerd is op de server; anders valt Aspose.Note terug op een standaardlettertype.  
- **Grote documenten** – Gebruik `Document.SaveOptions` om streaming in te schakelen, waardoor een hoog geheugenverbruik voor bestanden van meer dan 200 pagina's wordt voorkomen.  
- **Alinea‑uitlijning niet toegepast** – Controleer of je `ParagraphStyle.Alignment` op de `TextStyle` hebt ingesteld voordat je de `TextRun` toevoegt.

## Veelgestelde vragen  

**Q: Kan ik verschillende opmaakstijlen toepassen binnen dezelfde tekenreeks?**  
A: Ja. Door meerdere `TextRun`‑objecten te maken met verschillende `TextStyle`‑instellingen, kun je vet, kleur en grootte combineren in één alinea.

**Q: Is Aspose.Note geschikt voor het verwerken van grootschalige documentverwerkingstaken?**  
A: Absoluut. De bibliotheek verwerkt OneNote‑bestanden van honderden pagina's met een streaming‑model dat het geheugenverbruik laag houdt.

**Q: Kan ik Aspose.Note integreren met andere .NET‑bibliotheken of -frameworks?**  
A: Ja. Aspose.Note werkt naadloos met ASP.NET Core, WPF en elke .NET Standard‑compatibele bibliotheek.

**Q: Biedt Aspose.Note ondersteuning voor cloud‑gebaseerde documentverwerking?**  
A: Hoewel de core‑API lokaal draait, kun je het hosten in Azure Functions of AWS Lambda om cloud‑enabled services te bouwen.

**Q: Waar kan ik meer bronnen en ondersteuning voor Aspose.Note vinden?**  
A: Je kunt het [Aspose.Note forum](https://forum.aspose.com/c/note/28) verkennen voor community‑hulp en de documentatie raadplegen op de [website](https://reference.aspose.com/note/net/).

---

**Laatst bijgewerkt:** 2026-06-20  
**Getest met:** Aspose.Note 24.11 for .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Document maken met paginatitel in Aspose.Note](/note/net/loading-and-saving-operations/create-doc-with-page-title/)
- [Document opslaan in OneNote‑formaat in Aspose.Note](/note/net/loading-and-saving-operations/save-doc-to-onenote-format/)
- [Tekstmanipulatie in OneNote met Aspose.Note voor .NET](/note/net/text-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}