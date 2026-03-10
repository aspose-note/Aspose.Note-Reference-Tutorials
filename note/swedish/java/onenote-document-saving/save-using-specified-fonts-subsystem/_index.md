---
date: 2025-12-18
description: Lär dig hur du **sparar OneNote som PDF** med det angivna teckensnittssystemet
  i Java med Aspose.Note. Denna guide visar också hur du konverterar OneNote till
  PDF, laddar anpassade teckensnittsfiler och anger standardteckensnitt.
linktitle: Save OneNote as PDF Using Specified Fonts Subsystem
second_title: Aspose.Note Java API
title: Spara OneNote som PDF med system för specificerade teckensnitt
url: /sv/java/onenote-document-saving/save-using-specified-fonts-subsystem/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara OneNote som PDF med specificerat teckensnittssystem

## Introduktion

I många affärsscenarier behöver du **spara OneNote som PDF** samtidigt som du bevarar exakt hur de ursprungliga sidorna ser ut. Aspose.Note for Java gör detta enkelt genom att låta dig styra teckensnittssystemet under konverteringen. I den här handledningen går vi igenom tre praktiska sätt att **konvertera OneNote till PDF**, inklusive hur man **läser in anpassade teckensnittsfiler**, **anger ett standardteckensnitt**, och till och med **använder ett teckensnittsstömm** när teckensnittet inte finns på målmaskinen.

## Snabba svar
- **Vad betyder “spara OneNote som PDF”?** Det konverterar en .one-fil till en PDF samtidigt som layout och stil bevaras.  
- **Vilket API hanterar teckensnitt?** `DocumentFontsSubsystem` låter dig definiera ett standardteckensnitt eller läsa in en anpassad teckensnittfil/-ström.  
- **Behöver jag en licens för produktion?** Ja, en kommersiell Aspose.Note-licens krävs för icke‑testanvändning.  
- **Kan jag konvertera flera filer i ett batch?** Absolut – loopa bara över `Document`‑laddnings- och sparlogiken.  
- **Vilken Java-version krävs?** Java 15 eller senare (exemplet använder JDK 15).

## Vad är “spara OneNote som PDF” med ett teckensnittssystem?

Att spara OneNote som PDF med ett teckensnittssystem innebär att under konverteringsprocessen ersätter Aspose.Note eventuella saknade tecken med det teckensnitt du tillhandahåller. Detta garanterar att PDF-filen ser identisk ut på alla enheter, även när det ursprungliga teckensnittet inte är installerat.

## Varför styra teckensnittssystemet när du **konverterar OneNote till PDF**?

- **Konsekvent varumärkesprofil** – företagsdokument behåller exakt teckensnitt.  
- **Plattformsoberoende pålitlighet** – PDF-filer renderas likadant på Windows, macOS, Linux och mobila enheter.  
- **Minskade fel** – varningar om saknade teckensnitt försvinner, vilket ger ett rent resultat.

## Förutsättningar

### 1. Java Development Kit (JDK)

Se till att du har Java Development Kit (JDK) installerat på ditt system. Du kan ladda ner det från [här](https://www.oracle.com/java/technologies/javase-jdk15-downloads.html) om du inte redan har gjort det.

### 2. Aspose.Note för Java-biblioteket

Ladda ner och installera Aspose.Note för Java-biblioteket. Du kan ladda ner det från [webbplatsen](https://releases.aspose.com/note/java/).

## Importera paket

Se till att importera de nödvändiga paketen i ditt Java‑projekt:

```java
import com.aspose.note.Document;
import com.aspose.note.PdfSaveOptions;
import com.aspose.note.fonts.DocumentFontsSubsystem;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.nio.file.Paths;
```

Låt oss nu gå igenom varje exempel i flera steg för att bättre förstå processen.

## Hur man **sparar OneNote som PDF** med Document Fonts Subsystem och ett standardteckensnitt

### Steg 1: Spara med Document Fonts Subsystem med standardteckensnittsnamn

Detta steg visar hur man **sparar OneNote som PDF** på ett enkelt sätt genom att ange ett standardteckensnitt.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontName() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the default font.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFont("Times New Roman"));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontName_out.pdf", options);
}
```

I detta steg:
- OneNote-dokumentet laddas med Aspose.Note.
- **Standardteckensnittet** anges som **"Times New Roman"**.
- Dokumentet sparas i PDF-format med det valda teckensnittet.

### Steg 2: Spara med Document Fonts Subsystem med standardteckensnitt från fil

Här **läser vi in en anpassad teckensnittfil** och använder den som reserv när vi konverterar till PDF.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Specify the default font from the file.
    PdfSaveOptions options = new PdfSaveOptions();
    options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromFile(fontFile));

    // Save the document as PDF.
    oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromFile_out.pdf", options);
}
```

- Den **anpassade teckensnittfilen** `geo_1.ttf` **läses in från disk**.
- `usingDefaultFontFromFile` **anger standardteckensnitt från fil**, vilket säkerställer att PDF-filen använder detta teckensnitt när det ursprungliga saknas.
- Den resulterande PDF-filen bevarar det avsedda utseendet.

### Steg 3: Spara med Document Fonts Subsystem med standardteckensnitt från ström

Ibland kan teckensnittet lagras i en databas eller tas emot via ett nätverk. Detta exempel visar hur man **använder en teckensnittsstöm**.

```java
public static void SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream() throws IOException
{
    // Load the document into Aspose.Note.
    Document oneFile = new Document("missing-font.one");

    // Specify the path to the font file.
    String fontFile = "geo_1.ttf";

    // Load the font file as a stream.
    InputStream stream = new FileInputStream(fontFile);

    try
    {
        // Specify the default font from the stream.
        PdfSaveOptions options = new PdfSaveOptions();
        options.setFontsSubsystem(DocumentFontsSubsystem.usingDefaultFontFromStream(stream));

        // Save the document as PDF.
        oneFile.save("SaveUsingDocumentFontsSubsystemWithDefaultFontFromStream_out.pdf", options);
    }
    catch (Exception e)
    {
        stream.close();
    }
}
```

- Teckensnittsfilen öppnas som en **InputStream**, vilket är användbart när teckensnittet finns i en källa som inte är en fil.
- `usingDefaultFontFromStream` **använder en teckensnittsstöm** för att definiera reservteckensnittet.
- OneNote-filen sparas som PDF med det ström‑baserade teckensnittet.

## Vanliga problem och lösningar

| Problem | Varför det händer | Hur man åtgärdar |
|-------|----------------|------------|
| **Varningar om saknade tecknitt** | Källfilen .one refererar till ett teckensnitt som inte finns på maskinen. | Tillhandahåll ett standardteckensnitt via `usingDefaultFont`, `usingDefaultFontFromFile` eller `usingDefaultFontFromStream`. |
| **Filen för anpassat teckensnitt hittas inte** | Felaktig sökväg till `.ttf`‑filen. | Använd absoluta sökvägar eller verifiera den relativa sökvägen från arbetskatalogen. |
| **Strömmen stängs inte** | Undantag inträffar innan `close()` anropas. | Använd try‑with‑resources (`try (InputStream stream = ...) { ... }`) för automatisk stängning. |

## Vanliga frågor

**Q: Kan jag ange olika teckensnitt för olika delar av dokumentet?**  
A: Ja, du kan tillämpa anpassade teckensnittsinställningar på enskilda rich‑text‑element med `Font`‑klassen i Aspose.Note.

**Q: Är Aspose.Note kompatibel med alla versioner av OneNote?**  
A: Aspose.Note stödjer OneNote‑filer från de senaste skrivbords‑ och mobilversionerna, vilket ger bred kompatibilitet.

**Q: Hur kan jag hantera saknade teckensnitt när jag sparar dokument?**  
A: Använd teckensnittssystemmetoderna som visas ovan (`usingDefaultFont`, `usingDefaultFontFromFile`, `usingDefaultFontFromStream`) för att tillhandahålla en reserv.

**Q: Kan jag anpassa teckensnittsegenskaper som storlek och stil?**  
A: Absolut – API‑et låter dig ange storlek, stil, färg och andra attribut per körning.

**Q: Finns det en provversion av Aspose.Note för Java?**  
A: Ja, en gratis provversion kan laddas ner från Aspose‑webbplatsen.

## Slutsats

I den här handledningen lärde vi oss hur man **sparar OneNote som PDF** samtidigt som man styr teckensnittssystemet i Java med Aspose.Note. Genom att följa de tre tillvägagångssätten – ange ett standardteckensnitt, läsa in en anpassad teckensnittfil eller använda en teckensnittsstöm – kan du garantera enhetlig teckensnittsrepresentation över plattformar när du exporterar eller sparar dina OneNote‑dokument.

---

**Senast uppdaterad:** 2025-12-18  
**Testat med:** Aspose.Note for Java 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}