---
date: 2026-03-14
description: Lär dig hur du sparar OneNote‑dokument som TIFF‑filer med TIFF JPEG‑komprimering,
  TIFF PackBits‑komprimering eller CCITT Group 3 Fax i Java. Kontrollera bildkvalitet,
  filstorlek och färgläge med Aspose.Note.
linktitle: Save to TIFF Image Using TIFF JPEG Compression in OneNote
second_title: Aspose.Note Java API
title: Spara till TIFF-bild med TIFF JPEG‑komprimering i OneNote
url: /sv/java/onenote-document-saving/save-to-tiff-image-using-image-save-options/
weight: 21
---

 TIFF‑bild med TIFF JPEG‑komprimering i OneNote"

Similarly other headings.

Proceed.

Will translate bullet points.

Now code block placeholders remain.

Now produce final.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara till TIFF‑bild med TIFF JPEG‑komprimering i OneNote

## Introduktion

I den här handledningen kommer du att upptäcka **hur du sparar ett OneNote‑dokument till en TIFF‑fil med TIFF JPEG‑komprimering** samt två andra populära komprimeringsmetoder. Vi går igenom den nödvändiga konfigurationen, importerar de nödvändiga Java‑paketen och ger tydlig steg‑för‑steg‑kod för varje komprimeringsalternativ. När du är klar kan du kontrollera **TIFF‑bildkvalitet**, minska filstorleken och till och med skapa svart‑vita TIFF‑filer för fax‑liknande utskrifter.

## Snabba svar
- **Vad är TIFF JPEG‑komprimering?** En förlustkomprimeringsmetod som minskar TIFF‑filens storlek samtidigt som den visuella kvaliteten bevaras.  
- **Vilket bibliotek hanterar konverteringen?** Aspose.Note för Java.  
- **Behöver jag en licens?** En gratis provversion fungerar för testning; en licens krävs för produktion.  
- **Kan jag ändra bildkvaliteten?** Ja, sätt `quality`‑egenskapen på `ImageSaveOptions`.  
- **Är batch‑konvertering möjlig?** Absolut – loopa igenom dokumenten och applicera samma alternativ.

## Vad är TIFF JPEG‑komprimering?
TIFF JPEG‑komprimering lagrar bilddata i en TIFF‑behållare men använder JPEG:s förlustalgoritm för att krympa filen. Den är idealisk när du behöver en balans mellan **tiff image quality** och mindre filstorlek, särskilt för webb‑ eller arkiveringsscenarier.

## Varför använda olika TIFF‑komprimeringstyper?
- **JPEG** – Bra för fotografier; erbjuder justerbar kvalitet.  
- **PackBits** – Enkelt, förlustfritt run‑length‑kodning; användbart för grafik med stora enhetliga områden.  
- **CCITT Group 3 Fax** – Endast svart‑vitt; perfekt för skannade dokument och faxöverföring.  

Att välja rätt komprimering låter dig möta lagringsbegränsningar utan att offra den visuella noggrannhet som ditt program kräver.

## Konvertera One till TIFF med Aspose.Note
Om ditt mål är att **konvertera OneNote till TIFF**, täcker de tre metoderna nedan de vanligaste scenarierna. Varje metod läser in en `.one`‑fil, konfigurerar `ImageSaveOptions` och sparar resultatet som en `.tiff`‑fil.

## Förutsättningar

- Java Development Kit (JDK) installerat.  
- Aspose.Note för Java‑biblioteket tillagt i ditt projekt (Maven/Gradle eller manuellt JAR).  
- Grundläggande kunskap om Java‑syntax.

## Importera paket

Börja med att importera de nödvändiga Aspose.Note‑klasserna i din Java‑fil:

```java
import com.aspose.note.*;
import java.io.IOException;
import java.nio.file.Paths;
```

## Steg 1: Spara till TIFF med TIFF JPEG‑komprimering

Nedan är den kompletta metoden som läser in en OneNote‑fil och sparar den som en TIFF med JPEG‑komprimering. Justera `quality`‑värdet (0‑100) för att kontrollera **tiff image quality**.

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

### Så sparar du TIFF med JPEG‑komprimering i Java
1. Peka `dataDir` på mappen som innehåller din `.one`‑fil.  
2. Anropa `SaveToTiffUsingJpegCompression()` från din `main`‑metod eller tjänst.  
3. Den resulterande `.tiff`‑filen kommer att visas i samma katalog.

## TIFF PackBits‑komprimeringsöversikt

PackBits är en förlustfri komprimeringsalgoritm som fungerar bäst för bilder med stora områden av enfärgad färg. Den kallas ofta **tiff packbits compression** i dokumentation.

## Steg 2: Spara till TIFF med PackBits‑komprimering

Om du behöver ett förlustfritt alternativ är PackBits en enkel run‑length‑algoritm som fungerar bra för grafik med solida färger.

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
- Ingen kvalitetsinställning behövs eftersom PackBits är förlustfritt.

## Steg 3: Spara till TIFF med CCITT Group 3 Fax‑komprimering (Svart‑vit TIFF)

För fax‑liknande dokument vill du ofta ha en **black and white TIFF**. CCITT Group 3 ger hög komprimering för monokroma bilder.

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
|-------|----------|
| **Utdatafilen är större än förväntat** | Försök att minska JPEG‑`quality`‑värdet eller byt till PackBits om förlustfri är acceptabelt. |
| **Färger ser urvattnade ut** | Säkerställ att du inte oavsiktligt har satt `ColorMode.BlackAndWhite` när du behöver full färg. |
| **Fel: Unsupported image format** | Verifiera att du använder en aktuell version av Aspose.Note; äldre builds kan sakna vissa komprimerings‑enums. |
| **LicenseException vid körning** | Installera en giltig Aspose.Note‑licens (`License license = new License(); license.setLicense("Aspose.Note.Java.lic");`). |

## Vanliga frågor

**Q: Kan jag konvertera andra dokumenttyper (t.ex. PDF, DOCX) till TIFF med dessa alternativ?**  
A: Ja. Medan Aspose.Note fokuserar på OneNote‑filer, erbjuder Aspose.PDF, Aspose.Words och andra bibliotek liknande `ImageSaveOptions` för sina format.

**Q: Hur skiljer sig TIFF JPEG‑komprimering från en vanlig JPEG‑fil?**  
A: JPEG‑algoritmen är densamma, men bilddata lagras i en TIFF‑behållare, som kan innehålla flera sidor och rikare metadata.

**Q: Är det möjligt att batch‑processa många `.one`‑filer?**  
A: Absolut. Iterera över en katalog, anropa någon av de tre metoderna för varje fil och samla de resulterande TIFF‑filerna.

**Q: Kan jag styra DPI/resolution för den sparade TIFF‑filen?**  
A: Ja. Använd `options.setResolution(int dpi)` innan du sparar.

**Q: Stöder Aspose.Note asynkron bearbetning?**  
A: API‑et är synkront, men du kan omsluta anropen i Java:s `CompletableFuture` eller ett trådpool för parallell exekvering.

## Slutsats

Du har nu ett komplett **java tiff conversion**‑verktyg som låter dig spara OneNote‑dokument som TIFF‑filer med JPEG, PackBits eller CCITT Group 3 Fax‑komprimering. Justera kvalitet, färgläge och upplösning för att möta dina specifika **tiff image quality**‑krav, och integrera dessa metoder i batch‑arbetsflöden för maximal produktivitet.

---

**Senast uppdaterad:** 2026-03-14  
**Testat med:** Aspose.Note för Java 23.12 (senaste vid skrivtillfället)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}