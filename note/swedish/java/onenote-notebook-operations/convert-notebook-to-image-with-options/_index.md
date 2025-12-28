---
date: 2025-12-28
description: Lär dig hur du **konverterar OneNote till bild** och ställer in bildupplösning
  i Java med Aspose.Note. Denna steg‑för‑steg‑guide visar också hur du exporterar
  OneNote PNG‑filer.
linktitle: Convert OneNote to Image with Options - Aspose.Note
second_title: Aspose.Note Java API
title: Konvertera OneNote till bild med alternativ – Aspose.Note
url: /sv/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera OneNote till bild med alternativ - Aspose.Note

## Introduktion

I den här handledningen kommer du att lära dig hur du **konverterar OneNote till bild** med en mängd olika alternativ med hjälp av Aspose.Note för Java. Oavsett om du behöver en högupplöst PNG för rapportering eller en snabb JPEG‑miniatyr, visar stegen nedan exakt hur du uppnår detta och integrerar processen i dina Java‑applikationer.

## Snabba svar
- **Vad betyder “convert OneNote to image”?** Det omvandlar en hel OneNote‑anteckningsbok till rasterbildfiler (PNG, JPEG osv.).
- **Vilket format rekommenderas för förlustfri kvalitet?** PNG, eftersom det bevarar alla detaljer utan komprimeringsartefakter.
- **Hur kan jag ställa in bildens upplösning i Java?** Använd `ImageSaveOptions.setResolution(int dpi)` via `NotebookImageSaveOptions`.
- **Kan jag exportera en OneNote‑anteckningsbok som PNG i ett steg?** Ja, Aspose.Note erbjuder ett enda `save`‑anrop med lämpliga alternativ.
- **Behöver jag en licens för produktionsanvändning?** En kommersiell licens krävs för produktion; en gratis provversion finns tillgänglig för utvärdering.

## Vad är “convert OneNote to image”?
Att konvertera en OneNote‑anteckningsbok till en bild innebär att rendera varje sida i anteckningsboken som en bitmap‑fil. Detta är användbart för att skapa statiska förhandsgranskningar, arkivera innehåll eller bädda in anteckningssidors i rapporter där det ursprungliga OneNote‑formatet inte stöds.

## Varför använda Aspose.Note för Java?
- **Full kontroll** över utdataformat, upplösning och färgdjup.  
- **Ingen Microsoft Office‑beroende** – fungerar i alla server‑sidiga Java‑miljöer.  
- **Stöder komplexa anteckningsböcker** med inbäddade filer, bläck och rik text.

## Förutsättningar

1. **Java Development Kit (JDK)** – version 8 eller högre.  
2. **Aspose.Note for Java JAR‑filer** – ladda ner det senaste biblioteket från [here](https://releases.aspose.com/note/java/) och lägg till det i ditt projekts classpath.  

## Importera paket

Först importerar du de klasser vi behöver för att läsa in anteckningsboken och konfigurera bildutdata.

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Steg 1: Läs in anteckningsboken

Läs in den OneNote‑anteckningsbok du vill konvertera. Ersätt sökvägen med platsen för din `.onetoc2`‑fil.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

## Steg 2: Ställ in sparalternativ (How to **set image resolution java**)

Skapa en `NotebookImageSaveOptions`‑instans, välj utdataformat och ange önskad upplösning. I detta exempel använder vi PNG med 400 dpi.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

> **Proffstips:** För snabbare bearbetning av stora anteckningsböcker, sänk upplösningen (t.ex. 150 dpi). Höj den för utskriftsklara grafik.

## Steg 3: Spara anteckningsboken som bild (How to **export OneNote PNG**)

Definiera utdatafilens namn och anropa `save`. Samma alternativ tillämpas på varje sida i anteckningsboken.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

Koden ovan kommer att generera en PNG‑fil (eller en serie PNG‑filer, en per sida) med den upplösning du angav.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **OutOfMemoryError** på stora anteckningsböcker | Öka JVM‑heap‑storlek (`-Xmx2g`) eller minska upplösningen. |
| **Tomma sidor i utdata** | Säkerställ att anteckningsboken inte är lösenordsskyddad; använd `Notebook.load(path, password)` om det behövs. |
| **Ej stödd bildformat** | Använd endast `SaveFormat.Png`, `SaveFormat.Jpeg` eller `SaveFormat.Bmp` – andra format stöds inte för export av anteckningsböcker. |

## Vanliga frågor

**Q: Kan Aspose.Note hantera komplexa OneNote‑filer?**  
A: Ja, den bearbetar effektivt anteckningsböcker med inbäddade filer, bläckanteckningar och rik formatering.

**Q: Är Aspose.Note för Java enkelt att integrera i befintliga projekt?**  
A: Absolut. API‑et är enkelt och du behöver bara lägga till JAR‑filen i ditt classpath.

**Q: Kan jag anpassa bildutdata när jag konverterar en anteckningsbok?**  
A: Ja. Du kan ställa in upplösning, format och även färgdjup via `ImageSaveOptions`.

**Q: Erbjuder Aspose.Note support för utvecklare?**  
A: Ja. Aspose tillhandahåller omfattande dokumentation, forum och snabba supportkanaler.

**Q: Finns det en gratis provversion av Aspose.Note för Java?**  
A: Ja, du kan ladda ner en provversion från [here](https://releases.aspose.com/).

---

**Senast uppdaterad:** 2025-12-28  
**Testat med:** Aspose.Note 24.11 för Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}