---
date: 2026-06-20
description: Lär dig hur du skapar rich text-dokument och genererar OneNote-filer
  programatiskt med Aspose.Note för .NET. Steg‑för‑steg‑guide med code snippets.
keywords:
- create rich text document
- create onenote file
- set paragraph style
- apply font color
- create document outline
linktitle: Skapa Rich Text-dokument med Aspose.Note för .NET
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
title: Skapa Rich Text-dokument med Aspose.Note för .NET
url: /sv/net/loading-and-saving-operations/create-doc-with-rich-text/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa Rich Text-dokument med Aspose.Note för .NET

## Introduktion  

I den här handledningen kommer du att lära dig **hur man skapar ett rich text-dokument** med Aspose.Note för .NET och sedan spara det som en OneNote-fil. Oavsett om du behöver generera mötesanteckningar, projektöversikter eller något formaterat innehåll programatiskt, ger Aspose.Note dig full kontroll över textformatering, styckeformat och dokumentöversikter. Vi går igenom varje steg—från att importera namnrymder till att spara den slutliga *.one*-filen—så att du kan börja automatisera OneNote-generering redan idag.

## Snabba svar  

- **Vad gör Aspose.Note?** Den låter .NET‑utvecklare skapa, läsa och modifiera OneNote‑filer utan OneNote‑applikationen.  
- **Hur många formateringsalternativ stöds?** Över 30 textstilar, inklusive teckensnittsfamilj, storlek, färg, fetstil, kursiv och understrykning.  
- **Kan jag ställa in styckeformat programatiskt?** Ja – använd klassen `ParagraphStyle` för att definiera justering, indrag och avstånd.  
- **Vilket filformat produceras?** En standard *.one*-fil som öppnas i Microsoft OneNote, OneNote Online och mobila appar.  
- **Behöver jag en licens för utveckling?** En gratis tillfällig licens fungerar för utvärdering; en full licens krävs för produktionsanvändning.

## Vad är ett rich text-dokument?  

Ett **rich text-dokument** är en fil som lagrar text tillsammans med formateringsinformation såsom teckensnitt, färger och styckeformat. I Aspose.Note representeras detta av klassen `RichText`, som kan bifogas till titlar, konturer eller vilket sidobjekt som helst.

## Varför skapa en OneNote-fil med rich text?  

Att skapa OneNote‑filer med rich text låter dig producera professionellt formaterade anteckningar som behåller stil när de öppnas i någon OneNote‑klient. Detta är idealiskt för automatiserad rapportering, mötesprotokoll eller utbildningsmaterial där visuell hierarki och betoning förbättrar läsbarheten. Aspose.Notes förmåga att generera stora, flersidiga dokument utan att ladda allt i minnet gör det lämpligt för företagslösningar i stor skala.

## Förutsättningar  

1. **Utvecklingsmiljö** – Visual Studio 2022 eller någon kompatibel .NET‑IDE.  
2. **Aspose.Note för .NET** – Ladda ner från [download link](https://releases.aspose.com/note/net/).  
3. **Grundläggande C#‑kunskaper** – Du bör vara bekväm med klasser, objekt och inline‑kod.

## Hur importerar man nödvändiga namnrymder?  

Läs in de nödvändiga namnrymderna så att kompilatorn känner igen Aspose.Note‑typer. Att importera `System` och `System.Drawing` ger grundläggande .NET‑funktionalitet, medan Aspose.Note‑namnrymden (automatiskt refererad efter att biblioteket lagts till) ger åtkomst till dokument‑skapande klasser såsom `Document`, `Page` och `RichText`. Detta steg säkerställer att all efterföljande kod kompileras utan referensfel.  

```csharp
using Aspose.Note;
using Aspose.Note.Rendering;
using System.Drawing;
```

Nu har du åtkomst till `Document`, `Page`, `Title`, `RichText` och stilklasser.  

```csharp
using System;
using System.Drawing;
```

## Hur skapar man ett Document‑objekt?  

Instansiera klassen `Document` – detta objekt representerar hela OneNote‑filen i minnet. `Document`‑klassen är den översta behållaren som håller sidor, konturer och resurser, vilket låter dig bygga en komplett anteckningsbokstruktur programatiskt.  

```csharp
Document oneNoteDoc = new Document();
```

```csharp
Document doc = new Document();
```

## Hur initierar man ett Page‑objekt?  

Lägg till en `Page` i dokumentet; varje sida motsvarar en flik i OneNote. `Page`‑klassen modellerar en enskild OneNote‑sida, inklusive dess storlek, bakgrund och innehållshierarki, och ger en duk för titlar, konturer och andra element.  

```csharp
Page page = new Page(oneNoteDoc);
```

```csharp
Page page = new Page();
```

## Hur skapar man ett Title‑objekt?  

Ett `Title` innehåller sidans rubrik och visas högst upp på OneNote‑fliken. `Title` är en lättviktig behållare för en enda rad rich text som fungerar som sidans huvud, vilket gör det enkelt att ange ett tydligt, beskrivande namn för sidan.  

```csharp
Title pageTitle = new Title();
```

```csharp
Title title = new Title();
```

## Hur ställer man in textformateringsegenskaper?  

Definiera en standard `ParagraphStyle` som kommer att tillämpas på all efterföljande text om den inte åsidosätts. `ParagraphStyle` låter dig ange teckensnittsfamilj, storlek, färg, justering och avstånd på ett ställe, vilket säkerställer ett enhetligt utseende i hela dokumentet samtidigt som individuella åsidosättningar fortfarande är möjliga där det behövs.  

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

## Hur skapar man RichText med formatering för titeln?  

Konstruera ett `RichText`‑objekt, tilldela standardstilen och applicera sedan eventuell speciell formatering för titeln. `RichText` lagrar en samling `TextRun`‑objekt, där varje kan ha sin egen stil, vilket möjliggör fin‑granulär kontroll över teckensnitt, färg och andra attribut inom ett enda stycke.  

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

## Hur initierar man Outline‑ och OutlineElement‑objekt?  

`Outline` grupperar relaterat innehåll på en sida, medan `OutlineElement` representerar ett enskilt punkt- eller numrerat objekt. Dessa klasser låter dig bygga hierarkiska strukturer liknande den vänstra navigationspanelen i OneNote, vilket ger läsarna en tydlig, organiserad vy av notens sektioner.  

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

## Hur definierar man ytterligare textstilar?  

Skapa separata `ParagraphStyle`‑instanser för rubriker, underrubriker och vanliga stycken. Att använda distinkta stilar låter dig **set paragraph style** och **apply font color** konsekvent i hela dokumentet, vilket gör det enklare att upprätthålla visuell hierarki och förbättra läsbarheten.  

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

## Hur lägger man till formaterad text till RichText‑objektet?  

Lägg till flera `TextRun`‑objekt, var och en med sin egen stil, för att bygga ett rikligt formaterat stycke. Detta steg visar hur man **apply font color** och **set paragraph style** för olika sektioner av samma rad, vilket möjliggör blandade stilmeningar såsom fetstilade rubriker följda av färgad betoning.  

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

## Hur lägger man till Title och RichText till Outline?  

Fäst titeln och innehållet till `OutlineElement`, och lägg sedan till det i `Outline`. `OutlineElement` kan innehålla både en titel och en kropp av rich text, vilket bildar en komplett notsektion som visas som ett hopfällbart objekt i OneNotes navigationspanel.  

```csharp
outlineElement.Title = pageTitle;
outlineElement.RichText = contentRichText;
outline.Add(outlineElement);
```

```csharp
title.TitleText = titleText;
outlineElem.AppendChildLast(text);
```

## Hur lägger man till Outline till Page och Page till Document?  

Infoga konturen i sidan och lägg sedan till sidan i dokumenthierarkin. Detta skapar den slutgiltiga strukturen som OneNote kommer att rendera som en sida med en formaterad kontur, vilket säkerställer att alla element visas i rätt ordning när filen öppnas.  

```csharp
page.Add(outline);
oneNoteDoc.Add(page);
```

```csharp
outline.AppendChildLast(outlineElem);
page.AppendChildLast(outline);
doc.AppendChildLast(page);
```

## Hur sparar man Document som en OneNote‑fil?  

Ange utsökvägen och anropa `Save`. Filen får en *.one*-ändelse, klar att öppnas i OneNote. Sparandet genererar en **create onenote file** som bevarar all rich‑text‑formatering och kontur‑hierarki, vilket gör dokumentet omedelbart visas i någon OneNote‑klient.  

```csharp
oneNoteDoc.Save("QuarterlyReport.one");
```

```csharp
string dataDir = "Your Document Directory";
dataDir = dataDir + "CreateDocWithFormattedRichText_out.one";
doc.Save(dataDir);
```

## Vanliga problem och lösningar  

- **Missing fonts** – Se till att det teckensnitt du anger (t.ex. Calibri) är installerat på servern; annars faller Aspose.Note tillbaka på ett standardteckensnitt.  
- **Large documents** – Använd `Document.SaveOptions` för att aktivera streaming, vilket förhindrar hög minnesanvändning för filer över 200 sidor.  
- **Paragraph alignment not applied** – Verifiera att du har satt `ParagraphStyle.Alignment` på `TextStyle` innan du lägger till `TextRun`.

## Vanliga frågor och svar  

**Q: Kan jag applicera olika formateringsstilar inom samma textsträng?**  
A: Ja. Genom att skapa flera `TextRun`‑objekt med olika `TextStyle`‑inställningar kan du blanda fetstil, färg och storlek i ett enda stycke.  

**Q: Är Aspose.Note lämplig för att hantera dokumentbearbetningsuppgifter i stor skala?**  
A: Absolut. Biblioteket bearbetar flersidiga OneNote‑filer med en streaming‑modell som håller minnesanvändningen låg.  

**Q: Kan jag integrera Aspose.Note med andra .NET‑bibliotek eller ramverk?**  
A: Ja. Aspose.Note fungerar sömlöst med ASP.NET Core, WPF och alla .NET Standard‑kompatibla bibliotek.  

**Q: Ger Aspose.Note stöd för molnbaserad dokumentbearbetning?**  
A: Även om kärn‑API:et körs lokalt kan du hosta det i Azure Functions eller AWS Lambda för att bygga molnbaserade tjänster.  

**Q: Var kan jag hitta fler resurser och support för Aspose.Note?**  
A: Du kan utforska [Aspose.Note forum](https://forum.aspose.com/c/note/28) för community‑hjälp och få åtkomst till dokumentation på [website](https://reference.aspose.com/note/net/).  

**Senast uppdaterad:** 2026-06-20  
**Testat med:** Aspose.Note 24.11 för .NET  
**Författare:** Aspose  

## Relaterade handledningar

- [Skapa dokument med sidtitel i Aspose.Note](/note/net/loading-and-saving-operations/create-doc-with-page-title/)
- [Spara dokument i OneNote-format i Aspose.Note](/note/net/loading-and-saving-operations/save-doc-to-onenote-format/)
- [Textmanipulation i OneNote med Aspose.Note för .NET](/note/net/text-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}