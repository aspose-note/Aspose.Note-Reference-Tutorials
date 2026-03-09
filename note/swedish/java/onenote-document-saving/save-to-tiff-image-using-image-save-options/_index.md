---
date: 2025-12-17
description: Lär dig hur du sparar OneNote‑dokument som TIFF‑filer med TIFF‑JPEG‑komprimering,
  PackBits eller CCITT Group 3‑fax i Java. Kontrollera bildkvalitet, filstorlek och
  färgläge med Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Spara till TIFF-bild med TIFF JPEG-komprimering i OneNote
url: /sv/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara till TIFF‑bild med TIFF JPEG‑komprimering i OneNote

## Introduktion

I den här handledningen kommer du att upptäcka **hur du sparar ett OneNote‑dokument till en TIFF‑fil med TIFF JPEG‑komprimering** och två andra populära komprimeringsmetoder. Vi går igenom den nödvändiga konfigurationen, importerar de erforderliga Java‑paketen och tillhandahåller tydlig steg‑för‑steg‑kod för varje komprimeringsalternativ. I slutet kommer du att kunna kontrollera **TIFF‑bildkvalitet**, minska filstorleken och till och med skapa svart‑vita TIFF‑filer för fax‑liknande utskrifter.

## Snabba svar
- **Vad är TIFF JPEG‑komprimering?** En förlustkomprimeringsmetod som minskar TIFF‑filens storlek samtidigt som den visuella kvaliteten bevaras.  
- **Vilket bibliotek hanterar konverteringen?** Aspose.Note för Java.  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en licens krävs för produktion.  
- **Kan jag ändra bildkvaliteten?** Ja, sätt `quality`‑egenskapen på `ImageSaveOptions`.  
- **Är batch‑konvertering möjlig?** Absolut – loopa igenom dokumenten och tillämpa samma alternativ.

## Vad är TIFF JPEG‑komprimering?
TIFF JPEG‑komprimering lagrar bilddata i TIFF‑behållaren men använder JPEG:s förlustalgoritm för att minska filen. Det är idealiskt när du behöver en balans mellan **tiff‑bildkvalitet** och en mindre filstorlek, särskilt för webb‑ eller arkiveringsscenarier.

## Varför använda olika TIFF‑komprimeringstyper?
- **JPEG** – Bra för fotografier; erbjuder justerbar kvalitet.  
- **PackBits** – Enkelt, förlustfritt run‑length‑kodning; användbart för grafik med stora enhetliga områden.  
- **CCITT Group 3 Fax** – Endast svart‑vitt; perfekt för skannade dokument och faxöverföring.  

Genom att välja rätt komprimering kan du uppfylla lagringskraven utan att offra den visuella noggrannhet som krävs för din applikation.

## Förutsättningar

- Java Development Kit (JDK) installerat.  
- Aspose.Note för Java‑biblioteket tillagt i ditt projekt (Maven/Gradle eller manuellt JAR).  
- Grundläggande kunskap om Java‑syntax.

## Importera paket

Först, importera de nödvändiga Aspose.Note‑klasserna i din Java‑fil:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Steg 1: Spara till TIFF med TIFF JPEG‑komprimering

Nedan är den kompletta metoden som läser in en OneNote‑fil och sparar den som en TIFF med JPEG‑komprimering. Justera `quality`‑värdet (0‑100) för att kontrollera **tiff‑bildkvalitet**.

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

- `ImageSaveOptions` talar om för Aspose.Note att skriva ut en TIFF‑fil.  
- `setTiffCompression(TiffCompression.Jpeg)` väljer JPEG‑komprimering.  
- `setQuality(93)` (valfritt) finjusterar bildkvaliteten; lägre värden ger mindre filer.

### Så sparar du TIFF med JPEG‑komprimering i Java
1. Peka `dataDir` på mappen som innehåller din `.one`‑fil.  
2. Anropa `SaveToTiffUsingJpegCompression()` från din huvudmetod eller tjänst.  
3. Den resulterande `.tiff`‑filen kommer att visas i samma katalog.

## Steg 2: Spara till TIFF med PackBits‑komprimering

Om du behöver ett förlustfritt alternativ är PackBits en enkel run‑length‑algoritm som fungerar bra för grafik med enhetliga färger.

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

## Steg 3: Spara till TIFF med CCITT Group 3 Fax‑komprimering (svart‑vit TIFF)

För fax‑liknande dokument vill du ofta ha en **svart‑vit TIFF**. CCITT Group 3 ger hög komprimering för monokroma bilder.

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

- `setColorMode(ColorMode.BlackAndWhite)` tvingar en monokrom utskrift.  
- `setTiffCompression(TiffCompression.Ccitt3)` tillämpar den fax‑inriktade komprimeringen.

## Vanliga problem & tips

| Problem | Lösning |
|-------|----------|
| **Utdatafilen är större än förväntat** | Försök minska JPEG `quality`‑värdet eller byt till PackBits om förlustfri är acceptabelt. |
| **Färger ser urtvättade ut** | Se till att du inte oavsiktligt sätter `ColorMode.BlackAndWhite` när du behöver full färg. |
| **Fel: ej stödd bildformat** | Verifiera att du använder en recent version of Aspose.Note; äldre builds kan sakna vissa komprimerings‑enum. |
| **LicenseException vid körning** | Installera en giltig Aspose.Note‑licens (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Vanliga frågor

**Q: Kan jag konvertera andra dokumenttyper (t.ex. PDF, DOCX) till TIFF med dessa alternativ?**  
A: Ja. Aspose.Note fokuserar på OneNote‑filer, men Asposes andra bibliotek (PDF, Words) erbjuder liknande `ImageSaveOptions` för deras respektive format.

**Q: Hur skiljer sig TIFF JPEG‑komprimering från vanliga JPEG‑filer?**  
A: Bilddata lagras i en TIFF‑behållare, bevarar metadata och möjliggör flera sidor, medan komprimeringsalgoritmen förblir JPEG.

**Q: Är det möjligt att batch‑processa många `.one`‑filer?**  
A: Absolut. Loopa igenom en mapp, anropa någon av de tre metoderna per fil och samla de resulterande TIFF‑filerna.

**Q: Kan jag kontrollera DPI‑/upplösningen på den sparade TIFF‑filen?**  
A: Ja. Använd `options.setResolution(int dpi)` innan du sparar.

**Q: Stöder Aspose.Note asynkron bearbetning?**  
A: API‑et är i sig synkront, men du kan omsluta anrop i Java:s `CompletableFuture` eller trådpools för parallell körning.

## Slutsats

Du har nu ett komplett **java tiff‑konverterings**‑verktyg som låter dig spara OneNote‑dokument som TIFF‑filer med JPEG, PackBits eller CCITT Group 3 Fax‑komprimering. Justera kvalitet, färgläge och upplösning för att uppfylla dina specifika **tiff‑bildkvalitets**‑krav, och integrera dessa metoder i batch‑arbetsflöden för maximal produktivitet.

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.Note for Java 23.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}