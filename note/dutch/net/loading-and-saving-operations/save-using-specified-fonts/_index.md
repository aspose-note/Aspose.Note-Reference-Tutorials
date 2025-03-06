---
title: Bewaar het gebruik van gespecificeerde lettertypen in Aspose.Note
linktitle: Bewaar het gebruik van gespecificeerde lettertypen in Aspose.Note
second_title: Aspose.Note .NET API
description: Leer hoe u documenten met opgegeven lettertypen opslaat in Aspose.Note voor .NET. Pas lettertype-instellingen eenvoudig aan voor consistente documentopmaak.
weight: 28
url: /nl/net/loading-and-saving-operations/save-using-specified-fonts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bewaar het gebruik van gespecificeerde lettertypen in Aspose.Note

## Invoering

In deze zelfstudie leren we hoe u documenten kunt opslaan met opgegeven lettertypen in Aspose.Note voor .NET. We zullen verschillende methoden verkennen om dit stap voor stap te bereiken.

## Vereisten

Voordat we beginnen, zorg ervoor dat u over het volgende beschikt:

1.  Aspose.Note voor .NET: Zorg ervoor dat u Aspose.Note voor .NET hebt geïnstalleerd. Je kunt het downloaden van[hier](https://releases.aspose.com/note/net/).

2. Ontwikkelomgeving: u hebt een ontwikkelomgeving nodig die is ingesteld voor .NET-ontwikkeling.

## Naamruimten importeren

Laten we eerst de benodigde naamruimten importeren:

```csharp
using System;
using System.IO;

using Aspose.Note.Fonts;
using Aspose.Note.Saving;

```

## Stap 1: Opslaan met standaardlettertypenaam

In deze stap slaan we een document op met een opgegeven standaardlettertypenaam.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName()
{
    // Het pad naar de documentenmap.
    string dataDir = "Your Document Directory";

    // Laad het document in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Sla het document op als PDF met het opgegeven standaardlettertype.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFont("Times New Roman")
                          });
}
```

## Stap 2: Opslaan met standaardlettertype uit bestand

Laten we vervolgens een document opslaan met een standaardlettertype dat uit een bestand is geladen.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile()
{
    // Het pad naar de documentenmap.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Laad het document in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Sla het document op als PDF met het standaardlettertype geladen uit het bestand.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf";
    oneFile.Save(dataDir, new PdfSaveOptions()
                          {
                              FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromFile(fontFile)
                          });
}
```

## Stap 3: Opslaan met standaardlettertype uit Stream

Laten we ten slotte een document opslaan met een standaardlettertype dat uit een stream is geladen.

```csharp
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream()
{
    // Het pad naar de documentenmap.
    string dataDir = "Your Document Directory";

    string fontFile = Path.Combine(dataDir, "geo_1.ttf");

    // Laad het document in Aspose.Note.
    Document oneFile = new Document(Path.Combine(dataDir, "missing-font.one"));

    // Sla het document op als PDF met het standaardlettertype geladen vanuit de stream.
    dataDir = dataDir + "SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf";

    using (var stream = File.Open(fontFile, FileMode.Open, FileAccess.Read, FileShare.Read))
    {
        oneFile.Save(dataDir, new PdfSaveOptions()
                              {
                                  FontsSubsystem = DocumentFontsSubsystem.UsingDefaultFontFromStream(stream)
                              });
    }
}
```

## Conclusie

In deze zelfstudie hebben we onderzocht hoe u documenten kunt opslaan met opgegeven lettertypen in Aspose.Note voor .NET. Door deze stappen te volgen, kunt u de lettertype-instellingen aanpassen aan uw wensen, zodat uw documenten de gewenste opmaak krijgen.

## Veelgestelde vragen

### V1: Kan ik elk lettertype gebruiken voor het opslaan van documenten in Aspose.Note?

A1: Ja, u kunt elk lettertype opgeven voor het opslaan van documenten. Zorg ervoor dat het lettertypebestand toegankelijk is en correct is geladen.

### V2: Is Aspose.Note compatibel met verschillende documentformaten?

A2: Aspose.Note werkt voornamelijk met OneNote-documenten, maar biedt opties om op te slaan in verschillende formaten, waaronder PDF.

### V3: Hoe kan ik omgaan met ontbrekende lettertypen bij het opslaan van documenten?

A3: Aspose.Note biedt opties om standaardlettertypen te gebruiken voor het geval het opgegeven lettertype ontbreekt, waardoor een consistente documentopmaak wordt gegarandeerd.

### V4: Ondersteunt Aspose.Note het insluiten van lettertypen in uitvoerdocumenten?

A4: Ja, Aspose.Note maakt het insluiten van lettertypen mogelijk om de portabiliteit van documenten en consistente weergave op verschillende platforms te garanderen.

### V5: Waar kan ik verdere hulp krijgen met Aspose.Note?

 A5: Voor verdere hulp of technische ondersteuning kunt u terecht op de[Aspose.Note-forum](https://forum.aspose.com/c/note/28).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
