---
title: Opslaan met behulp van het opgegeven lettertypesubsysteem in OneNote
linktitle: Opslaan met behulp van het opgegeven lettertypesubsysteem in OneNote
second_title: Aspose.Note Java-API
description: Leer hoe u OneNote-documenten kunt opslaan met behulp van het opgegeven lettertypesubsysteem in Java met Aspose.Note. Zorg moeiteloos voor een consistente weergave van lettertypen op verschillende platforms.
type: docs
weight: 22
url: /nl/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## Invoering

Aspose.Note voor Java biedt robuuste mogelijkheden voor het werken met OneNote-documenten. Een veel voorkomende vereiste bij het werken met dergelijke documenten is ervoor zorgen dat de lettertypen goed worden onderhouden, vooral als het document moet worden geëxporteerd of opgeslagen in verschillende formaten zoals PDF. Deze zelfstudie leidt u door het proces van het opslaan van OneNote-documenten terwijl u het lettertypesubsysteem specificeert, waardoor een consistente en nauwkeurige weergave van tekst op verschillende platforms wordt gegarandeerd.

## Vereisten

Voordat we ingaan op de zelfstudie, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

### 1. Java-ontwikkelingskit (JDK)

 Zorg ervoor dat Java Development Kit (JDK) op uw systeem is geïnstalleerd. Je kunt het downloaden van[hier](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) als je dat nog niet hebt gedaan.

### 2. Aspose.Note voor Java-bibliotheek

 Download en configureer de Aspose.Note voor Java-bibliotheek. Je kunt het downloaden van de[website](https://releases.aspose.com/note/java/).

## Pakketten importeren

Zorg ervoor dat u de benodigde pakketten in uw Java-project importeert:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Laten we nu elk voorbeeld in meerdere stappen opsplitsen om het proces beter te begrijpen.

## Stap 1: Opslaan met behulp van het documentlettertypensubsysteem met standaardlettertypenaam

Deze stap laat zien hoe u een document in PDF-indeling opslaat met een opgegeven standaardlettertypenaam.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Laad het document in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Geef het standaardlettertype op.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Sla het document op als PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

In deze stap:
- Het OneNote-document wordt geladen met Aspose.Note.
- Het standaardlettertype is opgegeven als "Times New Roman".
- Het document wordt opgeslagen in PDF-formaat met het opgegeven lettertype.

## Stap 2: Opslaan met behulp van het documentlettertypen-subsysteem met standaardlettertype uit bestand

Deze stap laat zien hoe u een document in PDF-indeling kunt opslaan met een standaardlettertype dat uit een bestand is geladen.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Laad het document in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Geef het pad naar het lettertypebestand op.
    String fontFile = "geo_1.ttf";

    // Geef het standaardlettertype uit het bestand op.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Sla het document op als PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

In deze stap:
- Het lettertypebestand "geo_1.ttf" wordt geladen.
- Het standaardlettertype wordt opgegeven vanuit het geladen lettertypebestand.
- Het document wordt opgeslagen in PDF-formaat met het opgegeven lettertype.

## Stap 3: Opslaan met behulp van het documentlettertype-subsysteem met standaardlettertype uit Stream

Deze stap laat zien hoe u een document in PDF-indeling kunt opslaan met een standaardlettertype dat uit een stream is geladen.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Laad het document in Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Geef het pad naar het lettertypebestand op.
    String fontFile = "geo_1.ttf";

    // Laad het lettertypebestand als een stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Geef het standaardlettertype uit de stream op.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Sla het document op als PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

In deze stap:
- Het lettertypebestand "geo_1.ttf" wordt als stream geladen.
- Het standaardlettertype wordt opgegeven vanuit de geladen stream.
- Het document wordt opgeslagen in PDF-formaat met het opgegeven lettertype.

## Conclusie

In deze zelfstudie hebben we geleerd hoe u OneNote-documenten kunt opslaan met behulp van het opgegeven lettertype-subsysteem in Java met behulp van Aspose.Note. Door deze stappen te volgen, kunt u zorgen voor een consistente weergave van lettertypen op verschillende platforms bij het exporteren of opslaan van uw documenten.

## Veelgestelde vragen

### V1: Kan ik verschillende lettertypen opgeven voor verschillende delen van het document?

A1: Ja, u kunt verschillende lettertypen opgeven voor verschillende delen van het document met Aspose.Note voor Java.

### V2: Is Aspose.Note compatibel met alle versies van OneNote?

A2: Aspose.Note ondersteunt verschillende versies van OneNote, waardoor compatibiliteit tussen verschillende omgevingen wordt gegarandeerd.

### V3: Hoe kan ik omgaan met ontbrekende lettertypen bij het opslaan van documenten?

A3: Aspose.Note biedt opties om standaardlettertypen op te geven, zodat ontbrekende lettertypen effectief kunnen worden verwerkt tijdens het opslaan van documenten.

### V4: Kan ik de lettertype-eigenschappen, zoals grootte en stijl, aanpassen?

A4: Ja, u kunt lettertype-eigenschappen zoals grootte, stijl en kleur aanpassen met Aspose.Note voor Java.

### V5: Is er een proefversie beschikbaar voor Aspose.Note voor Java?

A5: Ja, u kunt een gratis proefversie van Aspose.Note voor Java krijgen via de website.