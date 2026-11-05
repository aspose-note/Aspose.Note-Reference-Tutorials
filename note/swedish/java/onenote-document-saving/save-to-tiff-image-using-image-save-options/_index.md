---
date: 2026-11-05
description: Lär dig hur du minskar TIFF-filens storlek när du konverterar OneNote-anteckningsböcker
  till TIFF i Java med Aspose.Note. Inkluderar JPEG, PackBits och svart‑vit TIFF-alternativ.
keywords:
- reduce tiff file size
- black white tiff
- tiff jpeg compression
- aspose note java
lastmod: 2026-11-05
linktitle: Hur man minskar TIFF-filens storlek när man konverterar OneNote i Java
og_description: Lär dig hur du minskar TIFF-filens storlek när du konverterar OneNote-anteckningsböcker
  till TIFF i Java med Aspose.Note. Inkluderar JPEG, PackBits och svart‑vit TIFF-alternativ.
og_image_alt: Developer guide showing OneNote to TIFF conversion with compression
  options in Java
og_title: Hur man minskar TIFF-filens storlek när man konverterar OneNote i Java
schemas:
- author: Aspose
  dateModified: '2026-11-05'
  description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  headline: How to reduce TIFF file size when converting OneNote in Java
  type: TechArticle
- description: Learn how to reduce TIFF file size when converting OneNote notebooks
    to TIFF in Java using Aspose.Note. Includes JPEG, PackBits and black‑white TIFF
    options.
  name: How to reduce TIFF file size when converting OneNote in Java
  steps:
  - name: Point `dataDir` to the folder containing your `.one` file.
    text: Point `dataDir` to the folder containing your `.one` file.
  - name: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
    text: Call `SaveToTiffUsingJpegCompression()` from your main method or service.
  - name: The resulting `.tiff` file will appear in the same directory.
    text: The resulting `.tiff` file will appear in the same directory.
  type: HowTo
- questions:
  - answer: Yes. While Aspose.Note focuses on OneNote files, Aspose.PDF, Aspose.Words,
      and other libraries provide similar `ImageSaveOptions` for their formats.
    question: Can I convert other document types (e.g., PDF, DOCX) to TIFF with these
      options?
  - answer: The JPEG algorithm is the same, but the image data lives inside a TIFF
      container, which can hold multiple pages and richer metadata.
    question: How does TIFF JPEG compression differ from a standard JPEG file?
  - answer: Absolutely. Iterate over a directory, call any of the three methods for
      each file, and collect the resulting TIFFs.
    question: Is it possible to batch‑process many `.one` files?
  - answer: Yes. Use `options.setResolution(int dpi)` before saving.
    question: Can I control the DPI/resolution of the output TIFF?
  - answer: The API itself is synchronous, but you can wrap calls in Java’s `CompletableFuture`
      or a thread pool for parallel execution.
    question: Does Aspose.Note support asynchronous processing?
  type: FAQPage
second_title: Aspose.Note Java API
tags:
- reduce tiff file size
- aspose.note
- java tiff conversion
- black white tiff
- image compression
title: Hur man minskar TIFF-filens storlek när man konverterar OneNote i Java
url: /sv/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man minskar TIFF-filstorlek vid konvertering av OneNote i Java

## Introduktion

I den här handledningen får du reda på hur du **minskar TIFF-filstorlek** när du konverterar OneNote‑anteckningsböcker till TIFF‑bilder med Aspose.Note för Java. Vi går igenom tre komprimeringsmetoder – TIFF JPEG, PackBits och CCITT Group 3 (svart‑vit TIFF) – visar hur du justerar bildkvalitet, styr färgläge och håller filstorlekar optimala för webb, arkivering eller fax‑liknande scenarier.

## Snabba svar
- **Vad är TIFF JPEG‑komprimering?** En förlustkomprimeringsmetod som minskar TIFF‑filstorlek samtidigt som den visuella kvaliteten bevaras.  
- **Vilket bibliotek hanterar konverteringen?** Aspose.Note för Java.  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en licens krävs för produktion.  
- **Kan jag ändra bildkvaliteten?** Ja, sätt `quality`‑egenskapen på `ImageSaveOptions`.  
- **Är batch‑konvertering möjlig?** Absolut – loopa igenom dokument och applicera samma alternativ.

## Översikt av TIFF JPEG‑komprimering

TIFF JPEG‑komprimering lagrar bilddata i en TIFF‑behållare men använder JPEG:s förlustalgoritm för att krympa filen. Den är idealisk när du behöver en balans mellan **tiff‑bildkvalitet** och mindre filstorlek, särskilt för webb‑ eller arkiveringsscenarier.

## Varför använda olika TIFF‑komprimeringstyper?

Du väljer komprimeringstyp baserat på innehåll och lagringsbehov: JPEG fungerar bäst för fotografier, PackBits ger förlustfri komprimering för grafik med stora enhetliga områden, och CCITT Group 3 levererar hög komprimeringsgrad för monokroma fax‑liknande dokument. Att välja rätt metod låter dig **minska TIFF‑filstorlek** utan att kompromissa med den visuella integriteten som din applikation kräver.

## Välja rätt komprimering

- **JPEG** – Justerbar kvalitet (0‑100) låter dig väga storlek mot detalj, perfekt för färgrika sidor.  
- **PackBits** – Förlustfri run‑length‑kodning; idealisk när varje pixel måste vara exakt.  
- **CCITT Group 3** – Endast monokrom; maximerar komprimeringen för skannad text eller fax‑dokument.  

## Konvertera OneNote till TIFF med Aspose.Note

Om ditt mål är att **konvertera OneNote till TIFF**, täcker de tre metoderna nedan de vanligaste scenarierna. Varje metod laddar en `.one`‑fil, konfigurerar `ImageSaveOptions` och sparar resultatet som en `.tiff`‑fil.

## Förutsättningar

- Java Development Kit (JDK) installerat.  
- Aspose.Note för Java‑biblioteket tillagt i ditt projekt (Maven/Gradle eller manuellt JAR).  
- Grundläggande kunskap om Java‑syntax.

## Importera paket

Klasserna `ImageSaveOptions`, `TiffCompression` och `ColorMode` är kärnan i konverterings‑API‑et.  

`ImageSaveOptions` definierar alternativen för att spara bilder, såsom format och komprimering.  
`TiffCompression` listar de stödjade TIFF‑komprimeringsalgoritmerna.  
`ColorMode` specificerar färgdjupet, t.ex. färg eller svart‑vit.  

```java
// Placeholder for import statements – keep your imports here
```

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Steg 1: spara till TIFF med TIFF JPEG‑komprimering

### Spara TIFF med JPEG‑komprimering i Java

Läs in OneNote‑filen, konfigurera `ImageSaveOptions` med JPEG‑komprimering, ange eventuellt `quality`‑värdet och anropa spara‑metoden. Detta tvåstegsmönster ger dig full kontroll över utdata‑storlek och visuell kvalitet.

1. Peka `dataDir` på mappen som innehåller din `.one`‑fil.  
2. Anropa `SaveToTiffUsingJpegCompression()` från din huvudmetod eller tjänst.  
3. Den resulterande `.tiff`‑filen kommer att visas i samma katalog.

```java
// Placeholder for the JPEG compression method implementation
```

```java
public static void SaveToTiffUsingJpegCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.Jpeg);
    options.setQuality(93);

    oneFile.save(Paths.get(dataDir,"SaveToTiffUsingJpegCompression.tiff").toString(), options);
}
```

**Förklaring**

- `ImageSaveOptions` talar om för Aspose.Note att output‑formatet ska vara en TIFF‑fil.  
- `setTiffCompression(TiffCompression.Jpeg)` väljer JPEG‑komprimering.  
- `setQuality(93)` (valfritt) finjusterar bildkvaliteten; lägre värden ger mindre filer.

## Översikt av TIFF PackBits‑komprimering

PackBits är en förlustfri komprimeringsalgoritm som fungerar bäst för bilder med stora områden av enhetlig färg. Den kallas ofta **tiff packbits compression** i dokumentationen.

## Spara TIFF med PackBits‑komprimering i Java

Om du behöver ett förlustfritt alternativ är PackBits en enkel run‑length‑algoritm som fungerar bra för grafik med solida färger. Konfigurera `ImageSaveOptions` med `TiffCompression.PackBits` och spara dokumentet.

```java
// Placeholder for the PackBits compression method implementation
```

```java
public static void SaveToTiffUsingPackBitsCompression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setTiffCompression(TiffCompression.PackBits);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingPackBitsCompression.tiff").toString(), options);
}
```

**Förklaring**

- `setTiffCompression(TiffCompression.PackBits)` byter komprimeringsmetod.  
- Ingen kvalitetsinställning behövs eftersom PackBits är förlustfri.

## Spara TIFF med CCITT Group 3‑komprimering i Java

För fax‑liknande dokument vill du ofta ha en **svart‑vit TIFF**. CCITT Group 3 ger hög komprimering för monokroma bilder. Ställ in färgläget till svart‑vit och välj CCITT 3‑komprimerings‑enum.

```java
// Placeholder for the CCITT Group 3 compression method implementation
```

```java
public static void SaveToTiffUsingCcitt3Compression() throws IOException {
    // The path to the documents directory.
    String dataDir = "Your Document Directory";

    // Load the document into Aspose.Note.
    Document oneFile = new Document(Paths.get(dataDir, "Aspose.one").toString());

    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
    options.setColorMode(ColorMode.BlackAndWhite);
    options.setTiffCompression(TiffCompression.Ccitt3);

    oneFile.save(Paths.get(dataDir, "SaveToTiffUsingCcitt3Compression.tiff").toString(), options);
}
```

**Förklaring**

- `setColorMode(ColorMode.BlackAndWhite)` tvingar en monokrom output.  
- `setTiffCompression(TiffCompression.Ccitt3)` applicerar den fax‑orienterade komprimeringen.

## Vanliga problem & tips

| Problem | Lösning |
|---------|---------|
| **Utdatafilen är större än förväntat** | Försök att sänka JPEG‑`quality`‑värdet eller byt till PackBits om förlustfri är acceptabelt. |
| **Färger ser urvattnade ut** | Säkerställ att du inte oavsiktligt har satt `ColorMode.BlackAndWhite` när du behöver full färg. |
| **Fel: Unsupported image format** | Verifiera att du använder en aktuell version av Aspose.Note; äldre builds kan sakna vissa komprimerings‑enum. |
| **LicenseException vid körning** | Installera en giltig Aspose.Note‑licens (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Vanliga frågor

**Q: Kan jag konvertera andra dokumenttyper (t.ex. PDF, DOCX) till TIFF med dessa alternativ?**  
A: Ja. Medan Aspose.Note fokuserar på OneNote‑filer, erbjuder Aspose.PDF, Aspose.Words och andra bibliotek liknande `ImageSaveOptions` för sina format.

**Q: Hur skiljer sig TIFF JPEG‑komprimering från en vanlig JPEG‑fil?**  
A: JPEG‑algoritmen är densamma, men bilddata lagras i en TIFF‑behållare, som kan innehålla flera sidor och rikare metadata.

**Q: Är det möjligt att batch‑processa många `.one`‑filer?**  
A: Absolut. Iterera över en katalog, anropa någon av de tre metoderna för varje fil och samla de resulterande TIFF‑filerna.

**Q: Kan jag styra DPI/upplösning på den sparade TIFF‑filen?**  
A: Ja. Använd `options.setResolution(int dpi)` innan du sparar.

**Q: Stöder Aspose.Note asynkron bearbetning?**  
A: API‑et självt är synkront, men du kan omsluta anropen i Java:s `CompletableFuture` eller ett trådpool för parallell exekvering.

## Slutsats

Du har nu ett komplett **Java‑TIFF‑konverterings‑verktyg** som låter dig **minska TIFF‑filstorlek** när du sparar OneNote‑dokument som TIFF‑filer med JPEG, PackBits eller CCITT Group 3‑fax‑komprimering. Justera kvalitet, färgläge och upplösning för att möta dina specifika krav, och integrera dessa metoder i batch‑arbetsflöden för maximal produktivitet.

---

**Senast uppdaterad:** 2026-11-05  
**Testat med:** Aspose.Note för Java 26.4 (senaste vid skrivtillfället)  
**Författare:** Aspose

## Relaterade handledningar

- [How to Render OneNote Page Image (JPEG) Using Save Format with Aspose.Note for Java](/note/java/onenote-document-saving/save-to-jpeg-image-using-save-format/)
- [Use Aspose.Note for Java to Save OneNote as PNG with Options – Convert Notebook to Image](/note/java/onenote-notebook-operations/convert-notebook-to-image-with-options/)
- [How to Export OneNote as Grayscale Image – Aspose.Note](/note/java/onenote-document-saving/save-to-grayscale-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}