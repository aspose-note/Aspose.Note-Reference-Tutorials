---
title: Spara med angivna teckensnittsundersystem i OneNote
linktitle: Spara med angivna teckensnittsundersystem i OneNote
second_title: Aspose.Note Java API
description: Lär dig hur du sparar OneNote-dokument med hjälp av specificerade teckensnittsundersystem i Java med Aspose.Note. Säkerställ konsekvent teckensnittsrepresentation över plattformar utan ansträngning.
type: docs
weight: 22
url: /sv/java/onenote-document-saving/save-using-specified-fonts-subsystem/
---
## Introduktion

Aspose.Note för Java ger robusta funktioner för att arbeta med OneNote-dokument. Ett vanligt krav när man arbetar med sådana dokument är att se till att typsnitten underhålls ordentligt, speciellt om dokumentet ska exporteras eller sparas i olika format som PDF. Den här handledningen guidar dig genom processen att spara OneNote-dokument samtidigt som du specificerar teckensnittsundersystemet, vilket säkerställer konsekvent och korrekt representation av text på olika plattformar.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar inställda:

### 1. Java Development Kit (JDK)

 Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner den från[här](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) om du inte redan har gjort det.

### 2. Aspose.Note för Java Library

 Ladda ner och ställ in Aspose.Note för Java-biblioteket. Du kan ladda ner den från[hemsida](https://releases.aspose.com/note/java/).

## Importera paket

Se till att importera de nödvändiga paketen i ditt Java-projekt:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Låt oss nu dela upp varje exempel i flera steg för att förstå processen bättre.

## Steg 1: Spara med dokumentteckensnittsundersystemet med standardteckensnittsnamn

Det här steget visar hur man sparar ett dokument i PDF-format med ett angivet standardteckensnittsnamn.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Ange standardteckensnittet.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Spara dokumentet som PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

I det här steget:
- OneNote-dokumentet laddas med Aspose.Note.
- Standardteckensnittet är specificerat som "Times New Roman".
- Dokumentet sparas i PDF-format med angivet typsnitt.

## Steg 2: Spara med dokumentteckensnittsundersystemet med standardteckensnitt från fil

Det här steget visar hur man sparar ett dokument i PDF-format med ett standardteckensnitt som laddas från en fil.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Ange sökvägen till teckensnittsfilen.
    String fontFile = "geo_1.ttf";

    // Ange standardteckensnittet från filen.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Spara dokumentet som PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

I det här steget:
- Teckensnittsfilen "geo_1.ttf" är laddad.
- Standardteckensnittet anges från den laddade teckensnittsfilen.
- Dokumentet sparas i PDF-format med angivet typsnitt.

## Steg 3: Spara med dokumentteckensnittsundersystemet med standardteckensnitt från Stream

Det här steget visar hur du sparar ett dokument i PDF-format med ett standardteckensnitt som laddas från en ström.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Ladda dokumentet i Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Ange sökvägen till teckensnittsfilen.
    String fontFile = "geo_1.ttf";

    // Ladda teckensnittsfilen som en ström.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Ange standardteckensnittet från strömmen.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Spara dokumentet som PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

I det här steget:
- Teckensnittsfilen "geo_1.ttf" laddas som en ström.
- Standardteckensnittet anges från den laddade strömmen.
- Dokumentet sparas i PDF-format med angivet typsnitt.

## Slutsats

I den här handledningen lärde vi oss hur man sparar OneNote-dokument med hjälp av specificerade teckensnittsundersystem i Java med Aspose.Note. Genom att följa dessa steg kan du säkerställa konsekvent teckensnittsrepresentation på olika plattformar när du exporterar eller sparar dina dokument.

## FAQ's

### F1: Kan jag ange olika typsnitt för olika delar av dokumentet?

S1: Ja, du kan ange olika teckensnitt för olika delar av dokumentet med Aspose.Note för Java.

### F2: Är Aspose.Note kompatibel med alla versioner av OneNote?

S2: Aspose.Note stöder olika versioner av OneNote, vilket säkerställer kompatibilitet mellan olika miljöer.

### F3: Hur kan jag hantera saknade teckensnitt när jag sparar dokument?

S3: Aspose.Note ger alternativ för att ange standardteckensnitt för att hantera saknade teckensnitt effektivt under dokumentsparandet.

### F4: Kan jag anpassa teckensnittsegenskaperna som storlek och stil?

S4: Ja, du kan anpassa teckensnittsegenskaper som storlek, stil och färg med Aspose.Note för Java.

### F5: Finns det en testversion tillgänglig för Aspose.Note för Java?

S5: Ja, du kan få en gratis provversion av Aspose.Note för Java från webbplatsen.