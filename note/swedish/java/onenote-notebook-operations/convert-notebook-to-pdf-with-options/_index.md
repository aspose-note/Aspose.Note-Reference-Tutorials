---
date: 2026-03-29
description: Konvertera OneNote-anteckningsböcker till PDF med alternativ, spara anteckningsboken
  som PDF och lägg till PDF-huvud och -fot med Aspose.Note för Java.
linktitle: Convert Notebook to PDF with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Konvertera OneNote till PDF med alternativ – Aspose.Note
url: /sv/java/onenote-notebook-operations/convert-notebook-to-pdf-with-options/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera OneNote till PDF med alternativ med Aspose.Note

## Introduktion

I den här handledningen kommer du att lära dig hur du **convert onenote to pdf** med full kontroll över resultatet. Aspose.Note for Java gör det enkelt att exportera OneNote‑anteckningsböcker till PDF, så att du kan **save notebook as pdf** samtidigt som du anpassar sidhuvuden, sidfötter och sidindelningsbeteende. Oavsett om du behöver generera rapporter, arkivera mötesanteckningar eller dela innehåll med användare som inte har OneNote, guidar den här guiden dig genom varje steg.

## Snabba svar
- **Vilket bibliotek hanterar konverteringen?** Aspose.Note for Java.
- **Kan jag lägga till ett sidhuvud eller en sidfot i PDF‑filen?** Ja – använd PDF‑sparalternativ för att infoga anpassade sidhuvuden/sidfötter.
- **Behöver jag en licens för produktion?** En kommersiell licens krävs för icke‑testanvändning.
- **Vilka Java‑versioner stöds?** Java 8 och senare.
- **Hur lång tid tar konverteringen?** Vanligtvis några sekunder för genomsnittliga anteckningsböcker.

## Vad är “convert onenote to pdf”?

Att konvertera OneNote till PDF innebär att ta en OneNote‑anteckningsbok (filen *.onetoc2*) och rendera varje sida som en PDF‑sida. Den resulterande PDF‑filen bevarar text, bilder och layout, vilket gör den läsbar på vilken enhet som helst utan att behöva OneNote.

## Varför använda Aspose.Note för att exportera onenote‑anteckningsbok till pdf?

- **Ingen Office‑installation krävs** – API‑et fungerar fristående.
- **Fin‑granulär kontroll** – du kan ställa in sidindelningsalgoritmer, bädda in teckensnitt och lägga till sidhuvuden/sidfötter.
- **Hög noggrannhet** – den visuella utformningen av den ursprungliga anteckningsboken bevaras.
- **Plattformsoberoende** – fungerar på Windows, Linux och macOS med vilken Java‑runtime som helst.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

1. Java Development Kit (JDK) – JDK 8 eller nyare installerat.
2. Aspose.Note for Java – ladda ner och installera från den [download link](https://releases.aspose.com/note/java/).
3. IDE (Integrated Development Environment) – IntelliJ IDEA, Eclipse eller NetBeans är populära val.

## Importera paket

Först måste du importera de nödvändiga paketen i ditt Java‑projekt. Dessa paket tillhandahåller klasserna och metoderna som krävs för att arbeta med OneNote‑dokument.

```java
import com.aspose.note.Notebook;
import java.io.IOException;
import com.aspose.note.KeepSolidObjectsAlgorithm;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookPdfSaveOptions;
import com.aspose.note.PdfSaveOptions;
```

## Steg 1: Ladda OneNote‑anteckningsboken

För att **convert onenote to pdf** måste du först ladda OneNote‑anteckningsboken. Se till att sökvägen till anteckningsboksfilen är korrekt angiven.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "Notizbuch �ffnen.onetoc2");
```

## Steg 2: Ange PDF‑sparalternativ

Aspose.Note erbjuder olika alternativ för att anpassa PDF‑utdata. Du kan ange alternativ som sidindelningsalgoritmer, sidhuvuds‑/sidfotsinställningar och mer.

```java
// Specify PDF save options
NotebookPdfSaveOptions notebookSaveOptions = new NotebookPdfSaveOptions();
PdfSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();
documentSaveOptions.setPageSplittingAlgorithm(new KeepSolidObjectsAlgorithm());
```

## Steg 3: Spara anteckningsboken som PDF

När du har laddat anteckningsboken och angett sparalternativen är det dags att **save the notebook as pdf**.

```java
dataDir = dataDir + "ExportNotebooktoPDFwithOptions_out.pdf";
// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|----------|
| PDF saknar bilder | Bilder lagrade som inbäddade objekt har inte laddats | Se till att anteckningsboksfilen och alla länkade resurser finns i samma katalog innan du laddar. |
| Sidhuvud/sidfötter visas inte | Sidhuvuds-/sidfotsalternativ har inte ställts in i `PdfSaveOptions` | Använd `documentSaveOptions.setHeaderFooter()` för att definiera innehållet innan du sparar. |
| Minnesfel vid stora anteckningsböcker | Hela anteckningsboken laddas in i minnet | Bearbeta anteckningsboken i sektioner eller öka JVM‑heap‑storleken (`-Xmx2g`). |

## Vanliga frågor

### Q1: Kan jag anpassa utseendet på PDF‑utdata?

A1: Ja, Aspose.Note erbjuder olika alternativ för att anpassa PDF‑utdata, inklusive sidhuvuds-/sidfotsinställningar, sidindelningsalgoritmer och mer.

### Q2: Är Aspose.Note kompatibel med alla versioner av OneNote?

A2: Aspose.Note stöder Microsoft OneNote 2010 och senare versioner.

### Q3: Erbjuder Aspose.Note en gratis provversion?

A3: Ja, du kan ladda ner en gratis provversion av Aspose.Note från [here](https://releases.aspose.com/).

### Q4: Var kan jag hitta dokumentation för Aspose.Note?

A4: Du kan hitta omfattande dokumentation för Aspose.Note [here](https://reference.aspose.com/note/java/).

### Q5: Hur kan jag få support för Aspose.Note?

A5: För teknisk hjälp eller frågor kan du besöka Aspose.Note‑supportforumet [here](https://forum.aspose.com/c/note/28).

## Ytterligare vanliga frågor

**Q: Hur lägger jag till ett anpassat PDF‑sidhuvud eller -sidfot?**  
A: Skapa ett `PdfHeaderFooterOptions`‑objekt, konfigurera texten eller bilderna, och tilldela det till `documentSaveOptions.setHeaderFooterOptions()` innan du anropar `save`.

**Q: Kan jag exportera endast utvalda sektioner av en anteckningsbok?**  
A: Ja – ladda anteckningsboken, hämta de önskade `Section`‑objekten och anropa `section.save()` med samma PDF‑alternativ.

**Q: Är det möjligt att kryptera den genererade PDF‑filen?**  
A: Absolut. Använd `documentSaveOptions.setEncryptionPassword("yourPassword")` för att skydda PDF‑filen.

**Q: Vilka prestandaöverväganden bör jag ha i åtanke?**  
A: För mycket stora anteckningsböcker, överväg att strömma utdata till en `FileOutputStream` och öka JVM‑heap‑storleken om du får ett `OutOfMemoryError`.

---

**Senast uppdaterad:** 2026-03-29  
**Testad med:** Aspose.Note for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}