---
title: Maak een OneNote-document en sla het op in HTML in Aspose.Note
linktitle: Maak een OneNote-document en sla het op in HTML in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u Microsoft OneNote-documenten kunt maken en opslaan in HTML-indeling in .NET-toepassingen met behulp van de Aspose.Note API. Volg onze uitgebreide tutorial met stapsgewijze voorbeelden.
type: docs
weight: 14
url: /nl/net/loading-and-saving-operations/create-onenote-doc-save-to-html/
---
## Invoering

Aspose.Note voor .NET is een krachtige API waarmee ontwikkelaars programmatisch met Microsoft OneNote-documenten kunnen werken in hun .NET-toepassingen. Met Aspose.Note kunt u moeiteloos OneNote-bestanden maken, manipuleren en converteren. In deze zelfstudie onderzoeken we hoe u een OneNote-document kunt maken en dit in HTML-indeling kunt opslaan met behulp van verschillende opties van de Aspose.Note voor .NET API.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

- Basiskennis van de programmeertaal C#.
- Visual Studio is op uw systeem geïnstalleerd.
-  Aspose.Note voor .NET API geïnstalleerd in uw project. Je kunt het downloaden van[hier](https://releases.aspose.com/note/net/).
- Bekendheid met de structuur van Microsoft OneNote-documenten.

## Naamruimten importeren

Voordat we ingaan op het codeergedeelte, importeren we eerst de benodigde naamruimten:

```csharp
using System;
using System.Drawing;
using System.Globalization;
using System.IO;

using Aspose.Note.Saving;
using Aspose.Note.Saving.Html;

```

Laten we nu elk voorbeeld in meerdere stappen opsplitsen en kijken hoe u een OneNote-document kunt maken en dit in HTML-indeling kunt opslaan met Aspose.Note voor .NET.

## Stap 1: Maak een OneNote-document met standaardopties

```csharp
public static void CreateAndSaveToHTMLUsingDefaultOptions()
{
    // Initialiseer het OneNote-document
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Standaardstijl voor alle tekst in het document.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Opslaan in HTML-formaat
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateOneNoteDocAndSaveToHTML_out.html");
    doc.Save(outputPath);

    Console.WriteLine("\nOneNote document created successfully.\nFile saved at " + outputPath);
}
```

In deze stap initialiseren we een nieuw OneNote-document, voegen een pagina met een titel toe en slaan deze op in HTML-indeling met behulp van standaardopties.

## Stap 2: Maak een specifiek paginabereik aan en sla het op in HTML

```csharp
public static void CreateAndSavePageRange()
{
    // Initialiseer het OneNote-document
    Document doc = new Document();
    Page page = doc.AppendChildLast(new Page());

    // Standaardstijl voor alle tekst in het document.
    ParagraphStyle textStyle = new ParagraphStyle { FontColor = Color.Black, FontName = "Arial", FontSize = 10 };
    page.Title = new Title()
    {
        TitleText = new RichText() { Text = "Title text.", ParagraphStyle = textStyle },
        TitleDate = new RichText() { Text = new DateTime(2011, 11, 11).ToString("D", CultureInfo.InvariantCulture), ParagraphStyle = textStyle },
        TitleTime = new RichText() { Text = "12:34", ParagraphStyle = textStyle }
    };

    // Opslaan in HTML-formaat
    string dataDir = "Your Document Directory";
    string outputPath = Path.Combine(dataDir, "CreateAndSavePageRange_out.html");
    doc.Save(outputPath, new HtmlSaveOptions { PageCount = 1, PageIndex = 0 });

    Console.WriteLine("\nOneNote document created successfully and saved as page range.\nFile saved at " + outputPath);
}
```

Hier laten we zien hoe u een document kunt maken en een specifiek paginabereik in HTML-indeling kunt opslaan.

## Stap 3: Opslaan als HTML in Memory Stream met ingebedde bronnen

```csharp
public static void SaveAsHTMLToMemoryStreamWithEmbeddedResources()
{
    // Laad het OneNote-document
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Geef HTML-opslagopties op
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportEmbedded,
        ExportFonts = ResourceExportType.ExportEmbedded,
        ExportImages = ResourceExportType.ExportEmbedded,
        FontFaceTypes = FontFaceType.Ttf
    };

    // Sla het document op in een geheugenstroom
    var memoryStream = new MemoryStream();
    document.Save(memoryStream, options);
}
```

Deze stap illustreert hoe u een OneNote-document in HTML-indeling met ingesloten bronnen (CSS, lettertypen en afbeeldingen) in een geheugenstroom kunt opslaan.

## Stap 4: Opslaan als HTML naar bestand met bronnen in afzonderlijke bestanden

```csharp
public static void SaveAsHTMLToFileWithResourcesInSeparateFiles()
{
    // Laad het OneNote-document
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Geef HTML-opslagopties op
    var options = new HtmlSaveOptions()
    {
        ExportCss = ResourceExportType.ExportAsStream,
        ExportFonts = ResourceExportType.ExportAsStream,
        ExportImages = ResourceExportType.ExportAsStream,
        FontFaceTypes = FontFaceType.Ttf
    };

    //Sla het document op in een HTML-bestand, waarbij de bronnen in afzonderlijke bestanden worden opgeslagen
    document.Save(Path.Combine(dataDir, "document_out.html"), options);
}
```

In deze stap slaan we een OneNote-document op in HTML-indeling, waarbij alle bronnen (CSS, lettertypen en afbeeldingen) in afzonderlijke bestanden worden opgeslagen.

## Stap 5: Opslaan als HTML in Memory Stream met callbacks om bronnen op te slaan

```csharp
public static void SaveAsHTMLToMemoryStreamWithCallBacksToSaveResources()
{
    // Geef de configuratie voor het opslaan van terugbelverzoeken op
    var savingCallbacks = new UserSavingCallbacks()
    {
        RootFolder = "documentFolder",
        CssFolder = "css",
        KeepCssStreamOpened = true,
        ImagesFolder = "images",
        FontsFolder = "fonts"
    };

    // Geef HTML-opslagopties op
    var options = new HtmlSaveOptions
    {
        FontFaceTypes = FontFaceType.Ttf,
        CssSavingCallback = savingCallbacks,
        FontSavingCallback = savingCallbacks,
        ImageSavingCallback = savingCallbacks
    };

    // Laad het OneNote-document
    string dataDir = "Your Document Directory";
    var document = new Document(Path.Combine(dataDir, "Aspose.one"));

    // Sla het document op in HTML-indeling met bronnen die worden beheerd door door de gebruiker gedefinieerde callbacks
    using (var stream = File.Create(Path.Combine(savingCallbacks.RootFolder, "document.html")))
    {
        document.Save(stream, options);
    }

    // Voeg handmatig gegevens toe aan de CSS-stream
    using (var writer = new StreamWriter(savingCallbacks.CssStream))
    {
        writer.WriteLine();
        writer.WriteLine("/* This line is appended to stream manually by user */");
    }
}
```

Hier laten we zien hoe u een OneNote-document in HTML-indeling kunt opslaan met bronnen die worden beheerd door door de gebruiker gedefinieerde callbacks.

## Conclusie

In dit artikel hebben we onderzocht hoe u met OneNote-documenten kunt werken en deze in HTML-indeling kunt opslaan met Aspose.Note voor .NET. Door de stapsgewijze handleiding te volgen, kunt u dit eenvoudig doen

 integreer deze functionaliteit in uw .NET-applicaties, zodat u OneNote-bestanden efficiënt kunt manipuleren.

## Veelgestelde vragen

### Vraag 1: Kan ik het uiterlijk van het opgeslagen HTML-bestand aanpassen?

A1: Ja, u kunt het uiterlijk aanpassen door de CSS-stylesheets te wijzigen die tijdens het conversieproces zijn gegenereerd.

### V2: Ondersteunt Aspose.Note conversie naar andere formaten dan HTML?

A2: Ja, Aspose.Note ondersteunt conversie naar verschillende formaten, zoals PDF, afbeeldingen en Microsoft Word-documenten.

### V3: Is Aspose.Note compatibel met .NET Core-applicaties?

A3: Ja, Aspose.Note is compatibel met zowel .NET Framework- als .NET Core-applicaties.

### V4: Kan ik tekst en afbeeldingen uit OneNote-documenten extraheren met Aspose.Note?

A4: Ja, u kunt tekst en afbeeldingen extraheren en diverse andere manipulaties uitvoeren met de Aspose.Note API.

### V5: Is er een proefversie beschikbaar voor het testen van Aspose.Note-functies?

 A5: Ja, u kunt een gratis proefversie downloaden van[hier](https://releases.aspose.com/).