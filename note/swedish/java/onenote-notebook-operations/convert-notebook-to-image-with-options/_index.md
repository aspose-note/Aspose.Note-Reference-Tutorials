---
date: 2026-03-24
description: Lär dig hur du sparar OneNote som PNG med alternativ med hjälp av Aspose.Note
  för Java. Den här guiden visar hur du exporterar OneNote som bild, ställer in bildupplösning
  i Java och konverterar OneNote till bild programatiskt.
linktitle: Convert Notebook to Image with Options in OneNote - Aspose.Note
second_title: Aspose.Note Java API
title: Spara OneNote som PNG med alternativ – Konvertera anteckningsbok till bild
  med Aspose.Note
url: /sv/java/onenote-notebook-operations/convert-notebook-to-image-with-options/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara OneNote som PNG med alternativ – Konvertera anteckningsbok till bild

## Introduktion

I den här handledningen kommer du att upptäcka hur du **sparar OneNote som PNG** med full kontroll över bildinställningarna med Aspose.Note för Java. Oavsett om du behöver exportera OneNote som bild för rapportering, generering av miniatyrer eller arkivering, så kommer stegen nedan att guida dig genom att konvertera en OneNote‑anteckningsbok till en bild medan du **ställer in bildupplösning i Java‑stil** för skarpa resultat.

## Snabba svar
- **Kan jag välja bildformatet?** Ja – du kan exportera till PNG, JPEG, BMP osv. genom att justera `SaveFormat`.
- **Hur kontrollerar jag bildkvaliteten?** Använd `ImageSaveOptions.setResolution()` för att definiera DPI (t.ex. 400 dpi).
- **Behöver jag en licens för produktion?** En kommersiell licens krävs för icke‑testanvändning.
- **Är API:et kompatibelt med Java 8+?** Absolut, Aspose.Note stödjer Java 8 och nyare.
- **Kan jag batch‑processa flera anteckningsböcker?** Ja – loopa igenom anteckningsböcker och tillämpa samma sparalternativ.

## Vad är “save onenote as png”?
Att spara OneNote som PNG innebär att konvertera hela anteckningsboken (eller specifika sektioner) till rasterbilder. PNG är förlustfri, vilket gör den idealisk för att bevara den visuella integriteten hos anteckningar, teckningar och inbäddade media.

## Varför exportera OneNote som bild med alternativ?
Att exportera OneNote som bild gör det möjligt att dela innehåll med användare som inte har OneNote installerat, bädda in anteckningar på webbsidor eller generera högupplösta PDF‑filer. Med Aspose.Note kan du **konvertera OneNote till bild** samtidigt som du anpassar upplösning, färgdjup och utdataformat – allt från Java‑kod.

## Förutsättningar

1. Java Development Kit (JDK) installerat på din maskin.  
2. Aspose.Note för Java JAR‑filer. Ladda ner biblioteket från [here](https://releases.aspose.com/note/java/) och lägg till det i ditt projekts classpath.

## Importera paket

Först, importera de klasser vi behöver:

```java
import java.io.IOException;

import com.aspose.note.ImageSaveOptions;
import com.aspose.note.Notebook;
import com.aspose.note.NotebookImageSaveOptions;
import com.aspose.note.SaveFormat;
```

## Steg‑för‑steg‑guide

### Steg 1: Ladda anteckningsboken
Ladda den OneNote‑anteckningsbok du vill konvertera.

```java
String dataDir = "Your Document Directory";
// Load a OneNote Notebook
Notebook notebook = new Notebook(dataDir + "test.onetoc2");
```

### Steg 2: Ställ in sparalternativ
Skapa en `NotebookImageSaveOptions`‑instans, välj PNG som format och **ställ in bildupplösning i Java‑stil**.

```java
NotebookImageSaveOptions notebookSaveOptions = new NotebookImageSaveOptions(SaveFormat.Png);

ImageSaveOptions documentSaveOptions = notebookSaveOptions.getDocumentSaveOptions();

documentSaveOptions.setResolution(400);
```

### Steg 3: Spara anteckningsboken som bild
Definiera utdatavägen och anropa `save`‑metoden. Detta kommer att **spara OneNote som PNG** med den upplösning du angav.

```java
dataDir = dataDir + "ExportNotebooktoImagewithOptions_out.png";

// Save the Notebook
notebook.save(dataDir, notebookSaveOptions);
```

## Vanliga problem & tips

- **Upplösning inte tillämpad:** Se till att du anropar `getDocumentSaveOptions()` innan du ställer in upplösningen; annars används standard‑DPI.  
- **Filen hittades inte:** Verifiera att `dataDir` pekar på rätt mapp och att `test.onetoc2` finns.  
- **Stora anteckningsböcker:** För mycket stora anteckningsböcker, överväg att öka JVM‑heap‑storleken (`-Xmx`) för att undvika `OutOfMemoryError`.

## Slutsats

Du vet nu hur du **sparar OneNote som PNG** med anpassade alternativ, effektivt **exporterar OneNote som bild** och **konverterar OneNote till bild** samtidigt som du styr upplösningen. Integrera dessa kodsnuttar i dina Java‑applikationer för att automatisera bearbetning av anteckningsböcker, generera miniatyrer eller skapa arkiveringskopior med perfekt visuell kvalitet.

## Vanliga frågor

### Q1: Kan Aspose.Note hantera komplexa OneNote‑filer?
A1: Ja, Aspose.Note kan hantera komplexa OneNote‑filer effektivt, vilket gör att du kan utföra olika operationer på dem programatiskt.

### Q2: Är Aspose.Note för Java lätt att integrera i befintliga projekt?
A2: Absolut! Aspose.Note för Java erbjuder ett enkelt API som är lätt att integrera i dina Java‑projekt, vilket sparar tid och ansträngning.

### Q3: Kan jag anpassa bildutdata när jag konverterar en anteckningsbok?
A3: Ja, Aspose.Note låter dig anpassa bildutdata genom att specificera alternativ som upplösning, format med mera.

### Q4: Erbjuder Aspose.Note support för utvecklare?
A4: Ja, Aspose erbjuder utmärkt support för utvecklare via sina forum och dokumentation, vilket säkerställer smidig integration och felsökning.

### Q5: Finns en gratis provversion av Aspose.Note för Java?
A5: Ja, du kan få en gratis provversion av Aspose.Note för Java från [here](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-03-24  
**Testat med:** Aspose.Note för Java (senaste)  
**Författare:** Aspose