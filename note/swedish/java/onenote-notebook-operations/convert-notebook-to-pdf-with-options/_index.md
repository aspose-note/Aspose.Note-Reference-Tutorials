---
date: 2025-12-28
description: Lär dig hur du exporterar OneNote till PDF med full kontroll med Aspose.Note
  för Java. Inkluderar exportalternativ för OneNote‑anteckningsbok till PDF och en
  Java‑guide för att konvertera anteckningsboken till PDF.
linktitle: How to Export OneNote to PDF with Options – Convert Notebook to PDF using
  Aspose.Note
second_title: Aspose.Note Java API
title: Hur man exporterar OneNote till PDF med alternativ – Konvertera anteckningsbok
  till PDF med Aspose.Note
url: /sv/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man exporterar OneNote till PDF med alternativ – Aspose.Note Java API

## Introduktion

I den här handledningen kommer du att lära dig **hur man exporterar OneNote till PDF** med anpassningsbara alternativ med hjälp av Aspose.Note för Java. Att konvertera en OneNote‑anteckningsbok till PDF är ett vanligt behov—oavsett om du behöver dela mötesanteckningar, arkivera dokumentation eller skapa utskrivbara rapporter. Med Aspose.Note är processen enkel, helt programmerbar och ger dig fin‑granulär kontroll över den resulterande PDF‑filen.

## Snabba svar
- **Vad gör API:t?** Det laddar en OneNote‑anteckningsbok och sparar den som en PDF med valfria inställningar.  
- **Vilket språk används?** Java – perfekt för server‑sida eller skrivbordsapplikationer.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Kan jag kontrollera sidlayouten?** Ja, du kan ställa in algoritmer för siduppdelning, sidhuvuden, sidfötter och mer.  
- **Är kodexemplet körbart?** Absolut – ersätt bara platshållarens sökväg med din anteckningsboks plats.

## Vad betyder “hur man exporterar OneNote till PDF”?

Att exportera OneNote till PDF innebär att omvandla den inhemska OneNote‑anteckningsboken (`*.onetoc2` och relaterade sektion‑filer) till ett portabelt, fast‑layout PDF‑dokument. Denna konvertering bevarar formatering, bilder och inbäddade objekt samtidigt som innehållet kan visas på vilken enhet som helst utan att kräva OneNote.

## Varför använda Aspose.Note för Java?

- **Ingen beroende av Microsoft Office** – fungerar på alla plattformar som kör Java.  
- **Rikliga PDF‑alternativ** – kontrollera siduppdelning, sidhuvuden/sidfötter och objekt‑hantering.  
- **Hög noggrannhet** – PDF‑utdata matchar nära det ursprungliga OneNote‑utseendet.  
- **Skalbar** – lämplig för batch‑bearbetning av tusentals anteckningsböcker.

## Förutsättningar

Innan vi börjar, se till att du har:

1. **Java Development Kit (JDK)** – version 8 eller högre.  
2. **Aspose.Note för Java** – ladda ner det från [nedladdningslänken](https://releases.aspose.com/note/java/).  
3. **En IDE** – IntelliJ IDEA, Eclipse eller NetBeans (valfritt).  
4. **En OneNote‑anteckningsbok** som du vill konvertera (t.ex. `Notizbuch öffnen.onetoc2`).

## Importera paket

Först importerar du de klasser som tillhandahåller anteckningsbokshantering och PDF‑sparfunktionalitet.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Steg 1: Ladda OneNote‑anteckningsboken

Ladda anteckningsboksfilen från disk. Ersätt `Your Document Directory` med den faktiska mappen som innehåller din `.onetoc2`‑fil.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Steg 2: Ange PDF‑spara‑alternativ

Här definierar du hur PDF‑filen ska genereras. Exemplet ställer in en algoritm för siduppdelning som håller solida objekt tillsammans, vilket är användbart när du har diagram eller tabeller som måste ligga på samma sida.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Steg 3: Spara anteckningsboken som PDF

Till sist skriver du ut anteckningsboken som en PDF‑fil. Utsökvägen kan vara vilken plats du föredrar.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|---------|
| **Fil ej hittad** | Felaktig `dataDir` eller filnamn. | Dubbelkolla sökvägen och säkerställ att anteckningsboksfilen finns. |
| **Saknade teckensnitt** | PDF‑rendering kräver samma teckensnitt som OneNote. | Installera de nödvändiga teckensnitten på servern eller bädda in dem via ytterligare Aspose‑alternativ. |
| **Stora anteckningsböcker orsakar OutOfMemoryError** | Hela anteckningsboken laddas in i minnet. | Bearbeta sektioner individuellt eller öka JVM‑heap‑storleken (`-Xmx`). |

## Slutsats

Vi har gått igenom **hur man exporterar OneNote till PDF** med Aspose.Note för Java, inklusive att ladda anteckningsboken, konfigurera PDF‑alternativ och spara resultatet. Genom att följa dessa steg kan du integrera konvertering från anteckningsbok till PDF i vilken Java‑applikation som helst, oavsett om det är ett skrivbordsverktyg, en webbtjänst eller ett batch‑bearbetnings‑backend.

## Vanliga frågor

### Q1: Kan jag anpassa utseendet på PDF‑utdata?

A1: Ja, Aspose.Note tillhandahåller olika alternativ för att anpassa PDF‑utdata, inklusive inställningar för sidhuvud/sidfötter, algoritmer för siduppdelning och mer.

### Q2: Är Aspose.Note kompatibel med alla versioner av OneNote?

A2: Aspose.Note stöder Microsoft OneNote 2010 och senare versioner.

### Q3: Erbjuder Aspose.Note en gratis provversion?

A3: Ja, du kan ladda ner en gratis provversion av Aspose.Note från [här](https://releases.aspose.com/).

### Q4: Var kan jag hitta dokumentation för Aspose.Note?

A4: Du kan hitta omfattande dokumentation för Aspose.Note [här](https://reference.aspose.com/note/java/).

### Q5: Hur kan jag få support för Aspose.Note?

A5: För teknisk hjälp eller frågor kan du besöka Aspose.Note supportforum [här](https://forum.aspose.com/c/note/28).

## Ytterligare vanliga frågor

**Q: Hur exporterar jag en OneNote‑anteckningsbok till PDF utan att förlora bilder?**  
A: Se till att `KeepSolidObjectsAlgorithm` är inställd (som visat) och att källanteckningsbokens bildfiler är åtkomliga i samma katalog.

**Q: Kan jag batch‑konvertera flera anteckningsböcker i ett körning?**  
A: Ja. Loop igenom en lista med anteckningsboks‑sökvägar, skapa en `Notebook` för varje, tillämpa samma `NotebookPdfSaveOptions` och anropa `save()`.

**Q: Finns det ett sätt att sätta PDF‑metadata (författare, titel) under konverteringen?**  
A: Använd `PdfSaveOptions.setMetadata()` för att definiera författare, titel, ämne och nyckelord innan du sparar.

**Q: Stöder API:t lösenordsskyddade PDF‑filer?**  
A: Du kan sätta ett lösenord på `PdfSaveOptions` via `setEncryptionPassword()` efter att ha konfigurerat andra alternativ.

**Q: Vilken version av Aspose.Note användes för den här handledningen?**  
A: Koden testades med Aspose.Note för Java 23.12.

---

**Senast uppdaterad:** 2025-12-28  
**Testad med:** Aspose.Note för Java 23.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}